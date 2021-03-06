# goit-markup-hw-08
Адаптивность

# Домашнее задание

- Создай репозиторий `goit-markup-hw-08`.
- Склонируй новый репозиторий и перенеси в него файлы предыдущей работы.
- Сверстай адаптивную версию всех страниц и элементов макета
  [домашнего задания #8](<https://www.figma.com/file/VQ02IIL57fc33U4GP1WEdf/Web-Studio-(Version-2.0)?node-id=1621%3A57>).
- Настрой `GitHub Pages` и добавь ссылку на живую страницу в шапку
  GitHub-репозитория.

## Критерии приёма работы

[Основные критерии прёма работы](./criteria.md)

### Дополнительные критерии

- Создан репозиторий `goit-markup-hw-08`.
- Использован препроцессор SASS.
- При написании стилей использован Mobile-first подход и медиа-функция
  `min-width`.
- В медиа-запросах отсутствует лишнее дублирование стилей.
- Стили необходимые только в определённом промежутке, закрыты в медиа-запросы
  `(min-width) and (max-width)`.
- Вёрстка выполнена относительно трёх точек перелома, как по макетам (480px,
  768px и 1200px).
- При просмотре страницы на любом устройстве, не появляется горизонтальная
  полоса прокрутки. Весь контент помещается в доступное горизонтальное
  пространство.
- Все фоновые и контентные растровые изображения - отзывчивые, и поддерживают
  экраны с плотностью пикселей `x1` и `x2`.
- Для контентных изображений использован отзывчивый элемент `<img>` c
  дескриптором `x`.

### Необязательные критерии

- Все контентные изображения - отзывчивые, поддерживают формат `webp` и
  плотность пикселей `x2`. При этом есть фолбек-изображения в альтернативном
  формате `jpg` или `png`.

### Скрипт для бургер меню

(() => {
  const menuBtnRef = document.querySelector("[data-menu-button]");
  const mobileMenuRef = document.querySelector("[data-menu]");

  menuBtnRef.addEventListener("click", () => {
    const expanded =
      menuBtnRef.getAttribute("aria-expanded") === "true" || false;

    menuBtnRef.classList.toggle("is-open");
    menuBtnRef.setAttribute("aria-expanded", !expanded);

    mobileMenuRef.classList.toggle("is-open");
  });
})();

