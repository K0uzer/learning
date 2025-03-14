# learning

### Список ссылок с вопросами

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

  ##Список задач для подготовки (JS):
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

  10. Напишите функцию, которая принимает на вход два массива чисел и возвращает новый массив, содержащий элементы, которые есть в обоих исходных массивах.

          const mergeArrays = (firstArr, secondArr) => [...firstArr, ...secondArr]
  
  11. Создайте функцию, которая принимает на вход число и возвращает его факториал.
  
          const searchFactorial = (num) =>
          {
              let resolve = 0
              for (let i = 1; i <= num; i++) resolve === 0 ? resolve = i * ++resolve : resolve = i * resolve
              return resolve
          }
  

  12. Реализуйте функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий только простые числа.

          const isPrimeNumber = (arr) => {
              return arr.filter((item) => {
                  if (item <= 1) return false; // 0 и 1 не являются простыми числами
                  for (let i = 2; i * i <= item; i++) { // Проверка до корня из item
                      if (item % i === 0) return false; // Если делится без остатка, не простое
                  }
                  return true; // Если не делится ни на одно число от 2 до sqrt(item), то простое
              });
          }
  
  
  13. Напишите функцию, которая принимает на вход две строки и возвращает true, если одна строка является анаграммой другой, и false в противном случае.
  
          const isAnagram = (firstWord, secondWord, countCoincide) => {
              firstWord.toLowerCase().split('').map((item) => secondWord.toLowerCase().split('').map(el => el === item ? countCoincide++ : countCoincide))
              return countCoincide === firstWord.length ? true : false
          }
  
  14. Создайте функцию, которая принимает на вход строку и возвращает объект, содержащий количество каждого символа в строке.

          const counterLetter = (word) =>
          {
              const result = {}
              word.split('').map((item) => Object.keys(result).includes(item) ? result[item] = result[item] + 1  : result[item] = 1)
              return result
          }
  
  15. Реализуйте функцию, которая принимает массив чисел и возвращает новый массив, содержащий только числа Фибоначчи.
    
          const getFibonacciArray = (array) => array.sort((a, b) => a - b).filter((item, index, array) => item === array[index - 1] + array[index - 2] )
  
  16. Напишите функцию, которая принимает на вход два массива объектов и возвращает новый массив, содержащий объединение элементов из обоих исходных массивов (без повторений).

          const getMergeFilteredArr = (arrFirst, arrSecond) => [...new Set([...arrFirst, ...arrSecond]
                .map((item) => item.string))]

  17. Напишите функцию, которая принимает на вход строку и возвращает новую строку без повторяющихся символов.

          const getStringWithoutDuplicateLetters = (word) => word.split('').reduce((acc, curr) => acc.includes(curr) ? acc : acc = [...acc, curr], [])

  18. Создайте функцию, которая принимает массив чисел и возвращает новый массив, содержащий только уникальные числа (без повторений).

          const getArrayUniqueNumbers = (arr) => {
            let result = []
            for (let unique of new Set(arr)) result = [...result, unique]
            return result
          }
  
  19. Реализуйте функцию, которая принимает на вход строку и возвращает true, если строка является палиндромом (читается одинаково в обоих направлениях), и false в противном случае.

          const isPalindrome = (word) => word.toLowerCase().split('').reverse().join('') === word.toLowerCase() ? true : false
  
  20. Напишите функцию, которая принимает на вход массив строк и возвращает новый массив, содержащий только строки, которые начинаются с определенной буквы.

          const getArrayWordStartOnlyALetter = (arr, letter) => arr.filter(item => item.split('').shift() === letter)
  
  22. Создайте функцию, которая принимает два числа и возвращает их наибольший общий делитель.

          ?????????????
  
  23. Реализуйте функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий суммы всех пар соседних элементов исходного массива.

          const getSumNeighborlyNumbers = (arr) => arr.reduce((acc, curr, index, arr) => [...acc, curr + arr[index++]], [])

  24. Напишите функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий только числа, которые являются четными.

          const getEvenNumbered = (arr) => arr.reduce((acc, curr) => curr % 2 === 0 ? [...acc, curr] : acc, [])

  25. Реализуйте функцию, которая принимает на вход строку и возвращает новую строку, в которой все символы инвертированы (например, "hello" станет "olleh").

          const getReverseString = (string) => string.split('').reverse().join('')

          или

          const getReverseString = (string) => string.split('').reduce((acc, curr) => curr + acc, '')

          или

          const getReverseStringForLoop = (string) => {
            let reversedString = '';
            for (let i = string.length - 1; i >= 0; i--) {
              reversedString += string[i];
            }
            return reversedString;
          }
          
  27. Создайте функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий только простые числа.

          ???????????????????????
  
  28. Напишите функцию, которая принимает на вход две строки и возвращает true, если они являются анаграммами (содержат одни и те же символы в разном порядке), и false в противном случае.

          const isAnagram = (firstStr, secondStr) => {
              if(firstStr.length !== secondStr.length) return false
              let count = 0
              for (let item of secondStr)
              {
                  if(firstStr.includes(item)) ++count
              }
              return count === firstStr.length ? true : false
          }

      или

            const isAnagram = (firstStr, secondStr) => {
              if (firstStr.length !== secondStr.length) {
                  return false;
              }
        
              const sortedFirstStr = firstStr.split('').sort().join('');
              const sortedSecondStr = secondStr.split('').sort().join('');
          
              return sortedFirstStr === sortedSecondStr;
            }
  
  30. Реализуйте функцию, которая принимает на вход массив строк и возвращает новый массив, содержащий только строки, длина которых больше заданного числа.

          const getFilteredArray = (arr) => arr.filter((item) => item.length > 5)
    
  31. Создайте функцию, которая принимает на вход число и возвращает true, если оно является числом Фибоначчи, и false в противном случае.

          const isFibonacciNumber = (number) =>
          {
              const fullSquareDec = Math.sqrt(5 * number**2 - 4)
              const fullSquareInc = Math.sqrt(5 * number**2 + 4)
              if (fullSquareDec === parseInt(fullSquareDec) || fullSquareInc === parseInt(fullSquareInc)) return true
              else return false
          }

  32. Создайте функцию, которая принимает на вход массив чисел и возвращает новый массив, в котором значения увеличены в два раза.

          const getSquareArr = (arr) => arr.map((item) => item*2)

  33. Напишите функцию, которая принимает на вход строку и возвращает количество гласных букв в этой строке.

          const getCountConsonantLetter = (str) => {
              const arrConsonant = ['а', 'о', 'у', 'ы', 'э', 'е', 'ё', 'и', 'ю', 'я']
              let countConsonant = 0
              for (let item of str)
              {
                  if (arrConsonant.includes(item.toLowerCase())) countConsonant++
              }
              return countConsonant
          }

      или

          const getCountVowelLetters = (str) => {
              const vowelRegex = /[аоуыэеёиюя]/gi; // Регулярное выражение для поиска гласных букв (регистронезависимо)
              const matches = str.match(vowelRegex); // Ищем совпадения с регулярным выражением в строке
              return matches ? matches.length : 0; // Возвращаем количество найденных гласных букв или 0, если совпадений не найдено
          }

  35. Напишите функцию, которая принимает на вход массив чисел и возвращает сумму всех элементов массива.

          const getSumArr = (arr) =>arr.reduce((acc, curr) => acc + curr, 0)
  
  36. Создайте функцию, которая принимает две строки и возвращает true, если они равны по длине, и false, если не равны.

          const isStringsEqualLength = (strFirst, strSecond) => strFirst.length === strSecond.length ? true : false

  37. Напишите функцию, которая принимает на вход массив чисел и возвращает новый массив, содержащий только уникальные числа (без повторений).

          const getArrayUniqueElements = (arr) => [...new Set(arr)]

  38. Реализуйте функцию, которая принимает на вход число n и возвращает строку из символов 'X' и 'O' длиной n, где каждые два символа повторяются поочередно.

          const getRepeatString = (number) =>
          {
              let result = 'ХО'
              for (let i = 0; i < number; i++) {
                  result = 'XO' + result
              }
              return result.repeat
          }

      или

          const getRepeatString = (number) => 'ХО'.repeat(number)

  40. Создайте функцию, которая принимает на вход два массива строк и возвращает новый массив, содержащий только те строки, которые есть и в первом, и во втором массивах.

          const getArrCoincidence = (arrFirst, arrSecond) => arrFirst.filter((item) => arrSecond.includes(item))

  41. Задача "Палиндром":
   Напишите функцию, которая принимает строку и возвращает true, если строка является палиндромом (читается одинаково слева направо и справа налево), и false в противном         случае.

          const isPalindrome = (word) => {
              let reverseWord = ''
              for (let i = word.length - 1; i >= 0; i--) {
                  reverseWord += word[i]
              }
              return reverseWord.toLowerCase() === word.toLowerCase()
          }

  42. Задача "Сжатие строки":
     Напишите функцию, которая принимает строку и возвращает новую строку, в которой повторяющиеся символы заменены на символ и количество повторений.

          const str = 'ffffффффф'

          const compressString = (word) =>
          {
              return word.split('').reduce((acc, curr, index, arr) =>
              {
                  if (acc.length === 0 || acc[acc.length - 2] != curr)  acc.push(curr, 1)
                  else acc[acc.length - 1]++
                  return acc
              }, []).join('')
          }
  
  43. Задача "Сортировка массива объектов":
     У вас есть массив объектов с различными свойствами. Напишите функцию, которая принимает этот массив и имя свойства, по которому нужно сортировать объекты. Функция должна возвращать массив объектов, отсортированных по указанному свойству.

          const getSortArrOfState = (arr, state) => arr.sort((itemFirst, itemSecond) => itemFirst[state] > itemSecond[state] ? 1 : -1)
  
  45. Задача "Рекурсивный поиск элемента в дереве объектов":
     Напишите функцию, которая рекурсивно ищет указанный элемент в дереве объектов (каждый объект может содержать другие объекты в свойстве children).

          const tree = {
              name: 'A',
              children: [
                  { name: 'B', children: [
                      { name: 'E', children: [] },
                      { name: 'F', children: [] }
                  ]},
                  { name: 'C', children: [
                      { name: 'G', children: [] }
                  ]},
                  { name: 'D', children: [
                      { name: 'H', children: [] },
                      { name: 'I', children: [
                          { name: 'J', children: [] }
                      ] }
                  ]}
              ]
          };

          const getSearchElement = (obj, target) => {
              if (obj.name === target) return obj
              if (obj.children) {
                  for (let child of obj.children) {
                      const result = getSearchElement(child, target)
                      if(result) return result
                  }
              }
          }

          console.log(getSearchElement(tree, 'G'))

----------------------------------------- Задачи с Promise ----------------------------------------------------------
  
  46. Задача "Реализация Promise.all()":
     Напишите свою собственную функцию, которая реализует функционал Promise.all(), принимая массив промисов и возвращая промис, который разрешится, когда все промисы из массива разрешатся.

          function customPromiseAll(promises) {
            return new Promise((resolve, reject) => {
                let results = [];
                let completed = 0;
                
                promises.forEach((promise, index) => {
                    promise.then(result => {
                        results[index] = result;
                        completed++;
                        
                        if (completed === promises.length) {
                            resolve(results);
                        }
                    }).catch(error => reject(error));
                });
            });
          }
    
          // Пример использования
          const promise1 = new Promise((resolve) => setTimeout(() => resolve(1), 1000));
          const promise2 = new Promise((resolve) => setTimeout(() => resolve(2), 2000));
          
          customPromiseAll([promise1, promise2])
              .then(results => {
                  console.log(results); // [1, 2]
              })
              .catch(error => {
                  console.error(error);
              });


  47. Создайте Promise, который успешно завершится через 2 секунды.

          const promise = new Promise((resolve) => setTimeout(resolve('done'), 2000)).then(data => console.log(data))
 
  48. Создайте Promise, который будет отклонен через 1 секунду.

          const promise = new Promise((resolve, reject) => setTimeout(reject('done'), 1000)).then(data => console.log(data))
          promise.catch((error) => console.log(error))  
 
  49. Создайте функцию, которая будет возвращать Promise с рандомным числом и после выполнения Promise выведет это число.

          const promise = new Promise((resolve, reject) => resolve((Math.random(0,1)).toFixed(1) * 10)).then(data => console.log(data))
  
  50. Напишите код, который реализует выполнение двух Promise параллельно и выведет результат, когда оба Promise завершатся.

          const promise1 = new Promise((resolve, reject) => resolve((Math.random(0,1)).toFixed(1) * 10)).then(data => console.log(data))

          const promise2 = new Promise((resolve, reject) => resolve((Math.random(0, 1)).toFixed(1) * 10)).then(data => console.log(data))
          
          const promAll = [promise1, promise2]
          
          Promise.all(promAll).then(data => data)
  
  51. Реализуйте функцию, которая будет возвращать Promise и будет выполняться через случайное время.

          function getPromise() {
            return new Promise((resolve) => setTimeout(() => resolve('done'), (Math.random()).toFixed(2) * 1000))
          }

          getPromise().then(data => console.log(data))
  
  52. Создайте Promise, который будет завершать выполнение через 3 секунды с определенным результатом.

          const prom = () => new Promise((resolve) => resolve('ok')).then((data) => console.log(data))
  
  53. Напишите функцию, которая принимает Promise и возвращает новый Promise, который будет отклонен через 2 секунды.

          function rejectAfterTwoSeconds(promise) {
            return new Promise((resolve, reject) => {
              setTimeout(() => {
                reject('no');
              }, 2000);
            });
          }

  
  54. Реализуйте Promise, который будет выполняться бесконечное время каждые 2 секунды.

          const prom = (pr) => new Promise((resolve, reject) => resolve('ok')).then((data) => setInterval(() => console.log(data), 2000))
  
  55. Напишите функцию, которая будет принимать массив Promise и возвращать новый Promise, который завершится, когда все Promise в массиве выполнены.

          const getNewPromise = (arrPromise) => Promise.all(arrPromise)
          getNewPromise(arr).then(data => console.log(data))
  
  56. Создайте Promise, который будет отклонен после 5 попыток.

          const getNewPromise = () =>
          {
              return new Promise((resolve, reject) =>
              {
                  let count = 0
                  while(count === 5) {
                      count++
                  }
                  reject('No')
              })
          }
          
          getNewPromise()
              .then(result => console.log(result))
              .catch(err => console.error(err))
  
  57. Напишите код, который будет принимать Promise и перехватывать ошибку, если ее нет.
  
  58. Реализуйте Promise, который будет завершать выполнение с рандомным результатом через определенное время.
  
  59. Напишите функцию, которая будет возвращать Promise и будет выполняться с определенным результатом через случайное время.
  
  60. Создайте Promise, который будет завершать выполнение со случайным результатом после 3 секунд.
  
  61. Напишите функцию, которая принимает Promise и возвращает новый Promise, который будет завершен через 2 секунды.
  
  62. Реализуйте Promise, который будет выполняться каждую секунду и завершаться после 10 итераций.
  
  63. Создайте код, который будет выполнять два Promise по очереди и выводить результат последовательно.
  
  64. Напишите функцию, которая принимает Promise и возвращает новый Promise, который будет успешно завершаться через 1 секунду.
  
  65. Реализуйте Promise, который будет завершен с ошибкой через 1 секунду.
  
  66. Напишите код, который будет выполнять 3 Promise параллельно и выведет результат, когда все Promise завершатся.

 ------------------------------------------------------------- Работа с объектами -----------------------------------------------------

   1. Создайте объект "автомобиль" с различными свойствами, такими как модель, год выпуска, цвет и т. д. Выведите информацию об автомобиле в консоль.

   2. Создайте объект "книга" с методом, который будет выводить краткое описание книги, включая название, автора и количество страниц.

   3. Напишите функцию-конструктор для создания объектов "студент", которая будет принимать имя, возраст и оценки. Создайте несколько экземпляров студента и выведите информацию о каждом из них.

   4. Создайте объект "кафе" с методами для добавления нового блюда, удаления блюда и вывода всего меню.

   5. Реализуйте объект "калькулятор", который будет иметь методы для выполнения основных математических операций (сложение, вычитание, умножение, деление).

   6. Напишите функцию logThis(), которая выводит в консоль значение this. Какое значение this будет выведено, если вызвать функцию напрямую (logThis()) и через метод объекта (obj.logThis())?

   7. Создайте объект person с методом sayHi(), который выводит в консоль "Привет, меня зовут имя!", где [имя] - это имя объекта person. Вызовите этот метод с использованием setTimeout, чтобы он вызывался через 1 секунду. Что будет выведено в консоль?
  
   8. У вас есть функция-конструктор User(name), которая создает объекты с именем name. Расширьте ее так, чтобы у всех объектов, созданных с помощью new User(name), был метод sayHi(), который выводит в консоль "Меня зовут имя". Создайте несколько объектов и вызовите метод sayHi() для каждого.
  
   9. Создайте объект counter, у которого есть свойства current (начальное значение 0) и методы increment() и getCurrent(). Метод increment() увеличивает значение current на 1, а метод getCurrent() возвращает текущее значение current. Привяжите методы к объекту counter с помощью метода bind().
  
   10. Создайте объект calculator, у которого есть свойства value (начальное значение 0) и методы add(number), subtract(number), multiply(number), divide(number). Эти методы изменяют значение value соответственно операции. Используйте call и apply для вызова этих методов с любым числом.
  
   11. Напишите функцию delay(func, ms), которая задерживает вызов func на ms миллисекунд. Используйте call или apply, чтобы реализовать это.
  
   12. Создайте функцию printUser() и объект user с свойством name. Используйте bind, чтобы связать printUser() с user и вызвать его.
  
   13. Создайте функцию saySomething(message), которая выводит сообщение в консоль. Создайте объект talker, который будет содержать свойство message и метод speak(), который будет вызывать saySomething() с сообщением из talker.message. Используйте bind, чтобы связать speak с saySomething.
  
   14. Напишите функцию logNumbers(), которая логирует числа от 1 до 5 через секунду с использованием bind.
  
   15. Создайте объект car с методом drive(), который выводит в консоль "Я еду на марка машины, скорость скорость км/ч". Создайте объект tesla как экземпляр car и используйте bind, чтобы изменить контекст drive() на tesla.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Средняя сложность

  1. Задача "Проверка на простое число":
   Напишите функцию, которая принимает число и возвращает true, если число является простым, и false в противном случае.
    
    const number = 7
    
    const isPrNumber = (number) => {
        let count = 0
        for(let index = 0; index <= number; index++) {
            if((number % index) === 0) count += 1
        }
        return count > 2 ? false : true
    }
    
    console.log(isPrNumber(number))

  2. Задача "Частота символов в строке":
     Напишите функцию, которая принимает строку и возвращает объект, содержащий частоту каждого символа в строке.

    const str = 'adawdjlkvmfnoerqwekp'
    
    const getQuantityLetters = (string) => {
        let quantityLetters = {}
        for(let element of string) {
            quantityLetters[element] ? quantityLetters[element]++ : quantityLetters[element] = 1
        }
        return quantityLetters
    }

    console.log(getQuantityLetters(str))    
  
  3. Задача "Объединение массивов без дубликатов":
     Напишите функцию, которая принимает несколько массивов и возвращает новый массив, содержащий уникальные элементы из всех входных массивов.

    let values1 = [1, 2, 3, 1, 4, 2, 5]
    let values2 = [1, 2, 3, 1, 4, 2, 6, 7]
    
    const getUniqueArray = (array1, array2) => [...new Set([...array1, ...array2])]
    
    console.log(getUniqueArray(values1, values2));
  
  4. Задача "Поиск пар элементов массива, сумма которых равна заданному числу":
     Напишите функцию, которая принимает массив чисел и целевое число, и возвращает массив из пар чисел, сумма которых равна целевому числу.

?????????????????????????
  
  5. Задача "Реализация каррирования":
     Напишите функцию, которая принимает функцию и возвращает новую функцию, которая вызывается либо с аргументами, либо частично (каррирование).


  
  6. Задача "Проверка на анаграмму":
     Напишите функцию, которая принимает две строки и возвращает true, если строки являются анаграммами, и false в противном случае.

         const isAnagram = (str1, str2) => {
            const sortedStr1 = str1.toLowerCase().split('').sort().join('');
            const sortedStr2 = str2.toLowerCase().split('').sort().join('');
            return sortedStr1 === sortedStr2;
         }
  
  8. Задача "Поиск наибольшего общего делителя":
     Напишите функцию, которая принимает два числа и возвращает их наибольший общий делитель.

          const getMaxCommuningDivisor = (numberFirst, numberSecond) => {
          let maxDivisor = 0
          for (let i = Math.min(numberFirst, numberSecond); i >= 1; i--) {
            if (numberFirst % i === 0 && numberSecond % i === 0) {
              maxDivisor = i
              break
            }
          }
          return maxDivisor
          }
  
  9. Задача "Фибоначчиева последовательность":
     Напишите функцию, которая возвращает n-ное число в последовательности Фибоначчи.

    const getNumberFibonacci = (quantityIteration) => {
        if(!quantityIteration) return 0
        if(quantityIteration === 1) return 1
        return getNumberFibonacci(quantityIteration-1) + getNumberFibonacci(quantityIteration-2)
    }

    console.log(getNumberFibonacci(10))
    
  10. Задача "Отсортировать массив 0 и 1":
     Напишите функцию, которая принимает массив, содержащий только числа 0 и 1, и возвращает этот массив, отсортированный по возрастанию.

    const arr = [0,1,0,1,0,1,1,1,0,0,0,1,0,1,0,0,0]

    const getFulterArr = (array) => {
      const zeros = []
      const ones = []
      for (let i = 0; i < array.length; i++) {
        if (array[i] === 0) {
          zeros.push(array[i])
        } else {
          ones.push(array[i])
        }
      }
      return zeros.concat(ones)
    }
    
    console.log(getFulterArr(arr))
  
  11. Задача "Расстановка ферзей на шахматной доске":
      Напишите функцию, которая решает задачу о расстановке восьми ферзей на шахматной доске, чтобы они не били друг друга.
  
  12. Задача "Поиск всех подстрок в строке":
      Напишите функцию, которая принимает строку и возвращает массив всех подстрок этой строки.
  
  13. Задача "Реализация бинарного поиска":
      Напишите функцию, которая принимает отсортированный массив и искомый элемент, и возвращает индекс элемента в массиве с использованием бинарного поиска.
  
  14. Задача "Поиск самой длинной подстроки без повторяющихся символов":
      Напишите функцию, которая принимает строку и возвращает самую длинную подстроку этой строки без повторяющихся символов.
  
  15. Задача "Глубокое сравнение объектов":
      Напишите функцию, которая рекурсивно сравнивает два объекта и возвращает true, если они идентичны, и false в противном случае.
  
  16. Задача "Реализация кэширующей функции":
      Напишите функцию, которая принимает другую функцию и возвращает новую функцию, кэширующую результат выполнения исходной функции для заданных аргументов.
  
  17. Задача "Проверка на совпадение последовательности чисел":
      Напишите функцию, которая принимает массив чисел и проверяет, содержатся ли в нем последовательно числа, начиная с 1.
  
  18. Задача "Подсчет количества вхождений слов в тексте":
      Напишите функцию, которая принимает текст и массив ключевых слов, и возвращает объект, содержащий количество вхождений каждого слова из массива в тексте.
  
  19. Задача "Реализация глубокого клонирования объекта":
      Напишите функцию, которая рекурсивно клонирует объект, включая вложенные объекты и массивы.
  
  20. Задача "Сумма отрицательных элементов массива":
      Напишите функцию, которая принимает массив чисел и возвращает сумму отрицательных элементов.
  
  21. Задача "Поиск наименьшей общей подстроки":
      Напишите функцию, которая принимает две строки и возвращает наименьшую общую подстроку этих строк.

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Сложные задачи

  1. Задача "Реализация сортировки графа":
     Напишите функцию, которая принимает граф (например, в виде списка смежности) и возвращает отсортированный граф по топологическому порядку.
  
  2. Задача "Поиск кратчайшего пути в графе":
     Напишите функцию, которая принимает граф и начальную и конечную вершины, и возвращает кратчайший путь между ними.
  
  3. Задача "Реализация алгоритма A":
     Напишите функцию, которая применяет алгоритм A для поиска кратчайшего пути в графе с учетом эвристической оценки.
  
  4. Задача "Поиск максимальной подстроки с нулями и единицами":
     Напишите функцию, которая принимает строку, состоящую только из нулей и единиц, и возвращает подстроку с наибольшим количеством нулей или единиц.
  
  5. Задача "Реализация алгоритма Бойера-Мура":
     Напишите функцию, которая применяет алгоритм Бойера-Мура для эффективного поиска подстроки в строке.
  
  6. Задача "Определение существования гамильтонова цикла":
     Напишите функцию, которая принимает граф и определяет, существует ли в нем гамильтонов цикл.
  
  7. Задача "Реализация алгоритма Дейкстры":
     Напишите функцию, которая применяет алгоритм Дейкстры для поиска кратчайшего пути в взвешенном графе.
  
  8. Задача "Поиск всех генераторов числа":
     Напишите функцию, которая принимает число и находит все его генераторы, т.е. числа, суммируя которые можно получить это число.
  
  9. Задача "Поиск всех перестановок множества":
     Напишите функцию, которая принимает множество элементов и возвращает все возможные перестановки этих элементов.
  
  10. Задача "Реализация алгоритма Флойда-Уоршелла":
      Напишите функцию, которая применяет алгоритм Флойда-Уоршелла для нахождения кратчайших путей между всеми парами вершин в графе.
  
  11. Задача "Проверка на существование мостов в графе":
      Напишите функцию, которая определяет, существуют ли в графе мосты (ребра, удаление которых делает граф несвязным).
  
  12. Задача "Реализация минимаксного алгоритма для игры":
      Напишите функцию, которая реализует алгоритм минимакс для определения оптимального хода в игре (например, крестики-нолики).
  
  13. Задача "Проверка на существование Эйлерова цикла":
      Напишите функцию, которая определяет, существует ли в графе Эйлеров цикл (цикл, который проходит по каждому ребру ровно один раз).
  
  14. Задача "Решение квадратного уравнения":
      Напишите функцию, которая принимает коэффициенты квадратного уравнения и возвращает его корни.
  
  15. Задача "Реализация алгоритма Эдмондса-Карпа":
      Напишите функцию, которая применяет алгоритм Эдмондса-Карпа для нахождения максимального потока в сети.
  
  16. Задача "Поиск всех сильно связанных компонент в графе":
      Напишите функцию, которая находит все сильно связанные компоненты в ориентированном графе.
  
  17. Задача "Реализация алгоритма Rabin-Karp":
      Напишите функцию, которая применяет алгоритм Rabin-Karp для эффективного поиска подстроки в строке с использованием хэширования.
  
  18. Задача "Определение наименьшего общего предка в дереве":
      Напишите функцию, которая находит наименьшего общего предка двух вершин в дереве.
  
  19. Задача "Реализация алгоритма Шеннона":
      Напишите функцию, которая применяет алгоритм Шеннона для сжатия данных.
  
  20. Задача "Поиск всех решений задачи о рюкзаке":
      Напишите функцию, которая находит все оптимальные решения задачи о рюкзаке, когда у вас есть набор предметов со значениями и весами, и ограничение на общий вес, который можно унести.
  
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

  
