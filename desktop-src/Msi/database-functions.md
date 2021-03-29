---
description: Этот материал предназначен для разработчиков, создающих собственные программы установки и разработчиков, желающих получить дополнительные сведения о таблицах базы данных установщика. Общие сведения об установщике см. в разделе About установщик Windows.
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: Функции базы данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a4233437d24944c8bb7fe5c7de6412e700022b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810750"
---
# <a name="database-functions"></a>Функции базы данных

Этот материал предназначен для разработчиков, создающих собственные программы установки и разработчиков, желающих получить дополнительные сведения о таблицах базы данных установщика. Общие сведения об установщике см. в разделе [About установщик Windows](about-windows-installer.md).

Для доступа к базе данных и процессу установки можно использовать функции доступа к установщику. Эти функции должны использоваться только пользовательскими действиями установки и средствами разработки. Для некоторых функций доступа к установщику требуются строки SQL для запроса к базе данных. Запросы должны соответствовать [синтаксису SQL](sql-syntax.md)установщика.

В этом разделе перечислены функции доступа к базе данных установщика по категориям.

## <a name="general-database-access-functions"></a>Общие функции доступа к базам данных



| Функция                                                             | Описание                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | Фиксирует изменения в базе данных.                                                          |
| [**мсидатабасежетпримарикэйс**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | Возвращает имена всех первичных ключевых столбцов.                                       |
| [**мсидатабасеистаблеперсистент**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | Возвращает перечисление, описывающее состояние таблицы.                                 |
| [**мсидатабасеопенвиев**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | Подготавливает запрос к базе данных и создает объект представления.                                    |
| [**Метод msigetactivedatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | Возвращает активную базу данных для установки.                                       |
| [**мсивиевжетколумнинфо**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | Возвращает имена или определения столбцов.                                                    |
| [**мсиопендатабасе**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | Открывает файл базы данных для доступа к данным.                                                  |
| [**мсивиевклосе**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | Освобождает результирующий набор для выполненного представления.                                           |
| [**мсивиевексекуте**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | Выполняет запрос представления и предоставляет необходимые параметры.                               |
| [**мсивиевфетч**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | Извлекает следующую последовательную запись из представления.                                       |
| [**мсивиевжетеррор**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | Возвращает ошибку, которая произошла в функции [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) . |
| [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | Обновляет выбранную запись.                                                               |



 

## <a name="database-management-functions"></a>Функции управления базами данных



| Функция                                                               | Описание                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | Создает сводные данные для существующего преобразования.           |
| [**мсидатабасеапплитрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | Применяет преобразование к базе данных.                               |
| [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | Экспортирует таблицу из открытой базы данных в текстовый файл архива.    |
| [**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | Создает файл преобразования различий между двумя базами данных. |
| [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | Импортирует таблицу с текстовым архивом установщика в открытую базу данных.   |
| [**мсидатабасемерже**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | Объединяет две базы данных вместе.                                   |
| [**мсижетдатабасестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | Возвращает состояние базы данных.                               |



 

## <a name="record-processing-functions"></a>Функции обработки записей



| Функция                                                 | Описание                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**мсикреатерекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | Создает новый объект Record с указанным числом полей.      |
| [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | Форматирует данные и свойства полей записи с помощью строки формата. |
| [**мсирекордклеардата**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | Задает для всех полей в записи значение null.                            |
| [**мсирекорддатасизе**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | Возвращает длину поля записи.                           |
| [**мсирекорджетфиелдкаунт**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | Возвращает число полей в записи.                       |
| [**мсирекорджетинтежер**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | Возвращает целочисленное значение из поля записи.                  |
| [**мсирекорджетстринг**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | Возвращает строковое значение поля записи.                     |
| [**мсирекордиснулл**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | Сообщает, имеет ли поле записи значение null.                         |
| [**мсирекордреадстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | Считывает байты из поля потока записи в буфер.           |
| [**мсирекордсетинтежер**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | Задает поле записи для целочисленного поля.                        |
| [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | Задает поле потока записей из файла.                         |
| [**мсирекордсетстринг**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | Копирует строку в указанное поле.                      |



 

## <a name="summary-information-property-functions"></a>Функции свойств сводных данных



| Функция                                                                 | Описание                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**мсижетсуммаринформатион**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | Получает маркер для сводного информационного потока базы данных установщика.    |
| [**мсисуммаринфожетпроперти**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | Возвращает одно свойство из сводных данных.                   |
| [**мсисуммаринфожетпропертикаунт**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | Возвращает число свойств в информационном потоке сводки.        |
| [**мсисуммаринфоперсист**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | Записывает измененные сводные данные обратно в информационный поток сводных данных. |
| [**мсисуммаринфосетпроперти**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | Задает одно свойство сводной информации.                            |



 

## <a name="installer-state-access-functions"></a>Функции доступа к состоянию установщика



| Функция                                               | Описание                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**мсижетлангуаже**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | Возвращает числовой язык текущей установки.   |
| [**мсижетластерроррекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | Возвращает запись об ошибке, которая была последней возвращена для вызывающего процесса. |
| [**мсижетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | Возвращает одно из логических состояний внутренней установки.    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | Возвращает значение свойства установщика.                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | Задает значение свойства установки.                 |
| [**мсисетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | Задает логическое состояние внутреннего обработчика.                      |



 

## <a name="installer-action-functions"></a>Функции действий установщика



| Функция                                             | Описание                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**мсидоактион**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | Выполняет Встроенное действие, настраиваемое действие или действие мастера пользовательских интерфейсов. |
| [**мсиевалуатекондитион**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | Вычисляет условное выражение, содержащее имена и значения свойств.  |
| [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | Отправляет в установщик запись об ошибке для обработки.                    |
| [**мсисекуенце**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | Выполняет последовательность действий.                                              |



 

## <a name="installer-location-functions"></a>Функции расположения установщика



| Функция                                     | Описание                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**мсижетсаурцепас**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | Возвращает полный исходный путь для папки в таблице Directory. |
| [**мсижеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | Возвращает полный целевой путь для папки в таблице Directory. |
| [**мсисеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | Задает полный целевой путь для папки в таблице Directory.    |



 

## <a name="installer-selection-functions"></a>Функции выбора установщика



| Функция                                                     | Описание                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**мсиенумкомпоненткостс**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | Перечисление места на диске, необходимого для установки компонента. |
| [**мсижеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | Получает состояние компонента.                                    |
| [**мсижетфеатурекост**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | Возвращает место на диске, необходимое для компонента.                        |
| [**мсижетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | Возвращает состояние компонента.                                         |
| [**мсижетфеатуревалидстатес**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | Возвращает допустимое состояние установки.                                  |
| [**мсисеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | Устанавливает компонент в указанное состояние.                             |
| [**мсисетфеатуреаттрибутес**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | Изменяет атрибуты компонента по умолчанию во время выполнения.            |
| [**мсисетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | Задает для компонента указанное состояние.                                 |
| [**мсисетинсталллевел**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | Задает уровень установки полной версии продукта.          |
| [**мсиверифидискспаце**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | Проверяет наличие достаточного места на диске.                                    |



 

## <a name="user-interface-functions"></a>Функции пользовательского интерфейса



| Функция                                           | Описание                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**мсиенаблеуипревиев**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | Включает режим предварительного просмотра пользовательского интерфейса.                             |
| [**мсипревиевбиллбоард**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | Отображает объявление с элементом управления ведущего приложения в отображаемом диалоговом окне. |
| [**мсипревиевдиалог**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | Отображает диалоговое окно как немодальное и неактивное.                         |



 

Все функции поддерживают вызовы ANSI и Unicode. Чтобы использовать эти функции, включите Мсикуери. h и свяжите с MSI. lib.

## <a name="installation-functions"></a>Функции установки

Помимо перечисленных выше функций доступа к базе данных, вы создаете пакет установки для приложения с помощью функций установщика, перечисленных в разделе Справочник по [функциям установщика](installer-function-reference.md) .

 

 



