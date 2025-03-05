#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#include <time.h>
#include <string.h>

// Константы
#define ARRAY_SIZE 19
#define SCREEN_WIDTH 60
#define COLOR_DEFAULT 7
#define COLOR_BLUE 11
#define COLOR_GREEN 10
#define COLOR_YELLOW 14
#define COLOR_BRIGHT_WHITE 15
#define COLOR_RED 12

// Структура для хранения локализованных строк
typedef struct {
    const char* title;
    const char* developer;
    const char* program_description[3];
    const char* choose_fill_method;
    const char* random_fill;
    const char* manual_fill;
    const char* your_choice;
    const char* generating;
    const char* array_generated;
    const char* enter_numbers;
    const char* element;
    const char* input_error;
    const char* no_negative;
    const char* first_negative;
    const char* array;
    const char* sum;
    const char* press_enter;
} Localization;

// Вспомогательные функции
void setColor(int color) {
    SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), color);
}

void printStyled(const char* text, int color, int centered) {
    setColor(color);
    if (centered) {
        int len = strlen(text);
        int padding = (SCREEN_WIDTH - len - 2) / 2;
        printf("|%*s%s%*s|\n", padding, "", text, padding + (len % 2), "");
    } else {
        printf("%s", text);
    }
    setColor(COLOR_DEFAULT);
}

void drawBorder() {
    setColor(COLOR_BLUE);
    printf("+%.*s+\n", SCREEN_WIDTH - 2, "-------------------------------------------------------");
    setColor(COLOR_DEFAULT);
}

// Функция для очистки буфера ввода
void clearInputBuffer() {
    while (getchar() != '\n');
}

// Функция для вывода заголовков блоков
void printHeader(const char* title) {
    drawBorder();
    printStyled(title, COLOR_YELLOW, 1);
    drawBorder();
}

// Функция для заполнения массива
void fillArray(float* array, int choice, const Localization* loc) {
    if (choice == 1) {
        // Автоматическое заполнение массива
        printStyled(loc->generating, COLOR_YELLOW, 0);
        printf("\n");
        
        for (int i = 0; i < ARRAY_SIZE; i++) {
            array[i] = ((float)rand() / RAND_MAX * 20.0) - 10.0;
            
            // Анимация
            printf("[");
            for (int j = 0; j <= i; j++) {
                setColor(COLOR_GREEN);
                printf("■");
            }
            for (int j = i + 1; j < ARRAY_SIZE; j++) {
                printf("□");
            }
            printf("] %d%%\r", (i + 1) * 100 / ARRAY_SIZE);
            Sleep(50);
        }
        printf("\n");
        printStyled(loc->array_generated, COLOR_GREEN, 0);
        printf("\n");
    } else {
        // Ручной ввод
        printStyled(loc->enter_numbers, COLOR_YELLOW, 0);
        printf("\n");
        
        for (int i = 0; i < ARRAY_SIZE; i++) {
            setColor(COLOR_BLUE);
            printf("%s %d: ", loc->element, i + 1);
            setColor(COLOR_BRIGHT_WHITE);
            
            if (scanf("%f", &array[i]) != 1) {
                setColor(COLOR_RED);
                printf("%s\n", loc->input_error);
                clearInputBuffer();
                i--; 
                continue;
            }
        }
    }
}

// Функция для отображения массива
void printArray(float* array) {
    printf("[ ");
    for (int i = 0; i < ARRAY_SIZE; i++) {
        if (array[i] < 0) {
            setColor(COLOR_RED);
        } else if (array[i] == 0) {
            setColor(COLOR_BRIGHT_WHITE);
        } else {
            setColor(COLOR_GREEN);
        }
        
        printf("%.2f", array[i]);
        setColor(COLOR_DEFAULT);
        
        if (i < ARRAY_SIZE - 1) printf(", ");
        
        // Перенос строки каждые 5 элементов
        if ((i + 1) % 5 == 0 && i < ARRAY_SIZE - 1) printf("\n  ");
    }
    printf(" ]\n");
}

int main() {
    // Настройка консоли на UTF-8
    SetConsoleCP(65001);
    SetConsoleOutputCP(65001);
    
    // Инициализация локализаций
    Localization en = {
        "=================================================",
        "Developer: Melnyk Dmytro",
        {
            "Program for calculating the sum of array elements",
            "located before the first negative element.",
            "If there are no negative elements, the result will be 0."
        },
        "Select array filling method:",
        "1 - Fill with random numbers",
        "2 - Enter manually",
        "Your choice: ",
        "\nGenerating random array...",
        "Array has been generated!",
        "Enter 19 real numbers:",
        "Element",
        "Input error. Please enter a valid number.",
        "\nThere are no negative elements in the array.",
        "\nThe first negative element is at position %d (value: %.2f).",
        "\nArray: ",
        "\nSum of elements before the first negative: %.2f\n\n",
        "Press Enter to continue..."
    };

    Localization ua = {
        "=====================================================",
        "Розробник: Мельник Дмитро",
        {
            "Програма для обчислення суми елементів масиву, розташованих",
            "до першого від'ємного елемента. Якщо від'ємні елементи",
            "відсутні, результат буде 0."
        },
        "Виберіть спосіб заповнення масиву:",
        "1 - Заповнити випадковими числами",
        "2 - Ввести вручну",
        "Ваш вибір: ",
        "\nГенерація випадкового масиву...",
        "Масив згенеровано!",
        "Введіть 19 дійсних чисел:",
        "Елемент",
        "Помилка вводу. Будь ласка, введіть дійсне число.",
        "\nУ масиві немає від'ємних елементів.",
        "\nПерший від'ємний елемент знаходиться на позиції %d (значення: %.2f).",
        "\nМасив: ",
        "\nСума елементів до першого від'ємного: %.2f\n\n",
        "Натисніть Enter для завершення..."
    };
    
    // Инициализация переменных
    Localization *loc;
    float array[ARRAY_SIZE];
    float sum = 0.0f;
    int found_negative = 0, i = 0;
    
    // Инициализация генератора случайных чисел
    srand(time(NULL));
    
    // Очистка экрана
    system("cls");
    
    // Выбор языка
    printHeader("Program by Melnyk Dmytro - Laboratory work #7");
    printStyled("Choose language / Виберіть мову:", COLOR_GREEN, 1);
    printStyled("1 - English", COLOR_DEFAULT, 1);
    printStyled("2 - Ukrainian / Українська", COLOR_DEFAULT, 1);
    printf("\n");
    
    printStyled("Your choice / Ваш вибір: ", COLOR_BRIGHT_WHITE, 0);
    int lang_choice;
    scanf("%d", &lang_choice);
    clearInputBuffer();
    
    // Установка локализации
    loc = (lang_choice == 1) ? &en : &ua;
    
    // Очистка экрана и вывод информации
    system("cls");
    
    // Информация о программе
    printHeader(loc->developer);
    for (i = 0; i < 3; i++) {
        printStyled(loc->program_description[i], COLOR_DEFAULT, 1);
    }
    drawBorder();
    printf("\n");
    
    // Выбор метода заполнения
    printStyled(loc->choose_fill_method, COLOR_GREEN, 1);
    printStyled(loc->random_fill, COLOR_DEFAULT, 1);
    printStyled(loc->manual_fill, COLOR_DEFAULT, 1);
    printf("\n");
    
    printStyled(loc->your_choice, COLOR_BRIGHT_WHITE, 0);
    int choice;
    scanf("%d", &choice);
    clearInputBuffer();
    
    // Заполнение массива
    fillArray(array, choice, loc);
    
    // Очистка экрана
    system("cls");
    
    // Вычисление суммы
    for (i = 0; i < ARRAY_SIZE; i++) {
        if (array[i] < 0) {
            found_negative = 1;
            break;
        }
        sum += array[i];
    }
    
    // Вывод результатов
    printHeader("RESULTS / РЕЗУЛЬТАТИ");
    
    if (!found_negative) {
        printStyled(loc->no_negative, COLOR_RED, 0);
        sum = 0;
    } else {
        setColor(COLOR_GREEN);
        printf(loc->first_negative, i + 1, array[i]);
        setColor(COLOR_DEFAULT);
    }
    
    printf("\n");
    drawBorder();
    
    // Вывод массива
    setColor(COLOR_BLUE);
    printf("%s\n", loc->array);
    setColor(COLOR_DEFAULT);
    printArray(array);
    
    // Вывод суммы
    printf("\n");
    drawBorder();
    setColor(COLOR_YELLOW);
    printf(loc->sum, sum);
    setColor(COLOR_DEFAULT);
    drawBorder();
    
    // Завершение программы
    printf("\n");
    printStyled(loc->press_enter, COLOR_BRIGHT_WHITE, 0);
    getchar();
    
    return 0;
}
