# learning

### Список ссылок с вопросами для собеседования

  ##JS:
  1. https://hackr.io/blog/javascript-interview-questions
  2. https://itvdn.com/ru/blog/article/300-js
  3. https://github.com/ninja-js/js-interview
  4. https://thecode.media/9-js-questions/
  5. https://ifellow.ru/media-center/voprosy-i-zadachi-na-sobesedovanii-js-v-2024-godu/
  6. https://habr.com/ru/articles/486820/
  7. https://www.guru99.com/javascript-interview-questions-answers.html

  ##REACT:
  1. https://github.com/AndrewMosh/react_interview_cheatsheet?tab=readme-ov-file#
  2. https://github.com/likezninjaz/react-ru-interview-questions
  3. https://dev.to/sakhnyuk/300-react-interview-questions-2ko4

  ##Задачи для собеса JS:
  1. https://purpleschool.ru/blog/pyat-zadach-dlya-javascript-razrabotchikov
  2. https://dev-station.ru/categories/js/taskbook/js-interview-tasks
  3. https://github.com/js-tasks-ru/js-coding-interview
  4. https://tproger.ru/translations/common-javascript-interview-challenges

  1. Напишите функцию, которая принимает строку как аргумент и возвращает эту строку в обратном порядке.

          const content = 'Привет, я Александр';
          const reversContent = (data) => data.split('').reverse().join('');
          console.log(reversContent(content));

  3. Реализуйте функцию, которая принимает массив чисел и возвращает сумму всех положительных чисел в массиве.

          const arrayPositiveNumberSum = (arr) =>
                  arr.reduce((acc, curr) => curr > 0 ? acc + curr : acc, 0)
  
  4. Создайте функцию, которая принимает на вход массив объектов и возвращает новый массив только с теми объектами, у которых определенное свойство имеет определенное значение.

          const filteredArray = (arr, from, before) => arr.filter((item) => item.index >= before && item.index <= from)

  6. Напишите функцию, которая принимает на вход массив строк и возвращает новый массив, содержащий только уникальные строки (без повторений).

          const arrayUniqueElementString = (arr) => [...new Set(arr.map((item) => item.toUpperCase()))]
  
  7. Реализуйте функцию, которая принимает строку и возвращает true, если строка является палиндромом, и false в противном случае.

          const isPalindrome = (word) => word.toLowerCase().split('').reverse().join('') === word.toLowerCase() ? true : false
  
  8. Напишите алгоритм сортировки массива чисел (например, сортировка пузырьком или быстрая сортировка).
     // сортировка пузырьком
     
          for (let i = 0; i < arr.length; i++) {
              for (let j = 0; j < arr.length; j++) {
                  if (arr[j] > arr[j + 1]) {
                      let tmp = arr[j];
                      arr[j] = arr[j + 1];
                      arr[j + 1] = tmp;
                  }
              }
          }
      // быстрая сортировка;
     
          const partition = (arr, start, end) => {
            const pivot = arr[end]; // Определяем опорный элемент
            let i = start; // Определяем индекс, по которому делим массив на две части
          
            for (let j = start; j <= end - 1; j++) {
              if (arr[j] <= pivot) {
                [arr[i], arr[j]] = [arr[j], arr[i]]; // Меняем значения переменных
                i++;
              }
            }
          
            [arr[i], arr[end]] = [arr[end], arr[i]]; // Меняем значения переменных
            return i;
          };
      
          const quickSort = (arr, start, end) => {
            if (start < end) { // Условия запуска рекурсии
              const pi = partition(arr, start, end); // Получаем индекс
      
              quickSort(arr, start, pi - 1);
              quickSort(arr, pi + 1, end);
            }
          };

  9. Напишите функцию, которая принимает на вход два массива чисел и возвращает новый массив, содержащий элементы, которые есть в обоих исходных массивах.

          const mergeArrays = (firstArr, secondArr) => [...firstArr, ...secondArr]
  
  10. Создайте функцию, которая принимает на вход число и возвращает его факториал.
  
          const searchFactorial = (num) =>
          {
              let resolve = 0
              for (let i = 1; i <= num; i++)
              {
                  resolve === 0 ? resolve = i * ++resolve : resolve = i * resolve
                  console.log(resolve)
              }
              return resolve
          }
  

  11. Реализуйте функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий только простые числа.

          const isPrimeNumber = (arr) => {
            return arr.filter((item) => {
                for (let i = 2; i <= item; i++) {
                    if(item % i !== 0 || item === i) return item
                    else if (item % i === 0) break
                }
            })
          }
  
  
  12. Напишите функцию, которая принимает на вход две строки и возвращает true, если одна строка является анаграммой другой, и false в противном случае.
  
          const isAnagram = (firstWord, secondWord, countCoincide) => {
              firstWord.toLowerCase().split('').map((item) => secondWord.toLowerCase().split('').map(el => el === item ? countCoincide++ :             countCoincide))
              return countCoincide === firstWord.length ? true : false
          }
  
  13. Создайте функцию, которая принимает на вход строку и возвращает объект, содержащий количество каждого символа в строке.

          const counterLetter = (word) =>
          {
              const result = {}
              word.split('').map((item) => Object.keys(result).includes(item) ? result[item] = result[item] + 1  : result[item] = 1)
              return result
          }
  
  15. Реализуйте функцию, которая принимает массив чисел и возвращает новый массив, содержащий только числа Фибоначчи.
    
          const getFibonacciArray = (array) => array.sort((a, b) => a - b).filter((item, index, array) => item === array[index - 1] + array[index - 2] )
  
  16. Напишите функцию, которая принимает на вход два массива объектов и возвращает новый массив, содержащий объединение элементов из обоих исходных массивов (без повторений).

  17. Напишите функцию, которая принимает на вход строку и возвращает новую строку без повторяющихся символов.

  18. Создайте функцию, которая принимает массив чисел и возвращает новый массив, содержащий только уникальные числа (без повторений).
  
  19. Реализуйте функцию, которая принимает на вход строку и возвращает true, если строка является палиндромом (читается одинаково в обоих направлениях), и false в противном случае.
  
  20. Напишите функцию, которая принимает на вход массив строк и возвращает новый массив, содержащий только строки, которые начинаются с определенной буквы.
  
  21. Создайте функцию, которая принимает два числа и возвращает их наибольший общий делитель.
  
  22. Реализуйте функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий суммы всех пар соседних элементов исходного массива.

  23. Напишите функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий только числа, которые являются четными.

  24. Реализуйте функцию, которая принимает на вход строку и возвращает новую строку, в которой все символы инвертированы (например, "hello" станет "olleh").
  
  25. Создайте функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий только простые числа.
  
  26. Напишите функцию, которая принимает на вход две строки и возвращает true, если они являются анаграммами (содержат одни и те же символы в разном порядке), и false в противном случае.
  
  27. Реализуйте функцию, которая принимает на вход массив строк и возвращает новый массив, содержащий только строки, длина которых больше заданного числа.
  
  28. Создайте функцию, которая принимает на вход число и возвращает true, если оно является числом Фибоначчи, и false в противном случае.

  29. Создайте функцию, которая принимает на вход массив чисел и возвращает новый массив, в котором значения увеличены в два раза.

  30. Напишите функцию, которая принимает на вход строку и возвращает количество гласных букв в этой строке.

  ##Задачи для собеса REACT:
  1. Создайте компонент в React, который выводит "Hello, World!" на экран.
  2. Реализуйте компонент, который отображает список элементов из массива.
  3. Создайте форму в React, которая позволяет пользователю вводить текст и сохранять его в состоянии компонента.
  4. Реализуйте функциональность добавления и удаления элементов из списка с использованием состояния.
  5. Создайте компонент, который загружает данные с сервера и отображает их на странице.
  6. Реализуйте функциональность фильтрации списка элементов на основе введенного пользователем текста.
  7. Создайте компонент, который отображает модальное окно с возможностью закрытия по нажатию на кнопку.
  8. Реализуйте форму ввода данных с валидацией полей (например, проверкой на заполненность).
  9. Создайте компонент, который работает с жизненным циклом React (например, componentDidMount, componentDidUpdate).
  10. Разработайте SPA (Single Page Application) с использованием React Router для навигации по разным страницам.

  
