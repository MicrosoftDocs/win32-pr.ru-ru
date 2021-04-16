---
title: Пример Контекстпопуп
description: В этом примере кода демонстрируется разметка и код, необходимые для реализации приложения ленты Windows с помощью Контекстпопупс.
ms.assetid: f334dbfc-710a-4652-b914-a668ae36aecd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ff2f66b27c3fb244181a779718079b3f992b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710495"
---
# <a name="contextpopup-sample"></a>Пример Контекстпопуп

В этом примере кода демонстрируется разметка и код, необходимые для реализации приложения ленты Windows с помощью Контекстпопупс.

-   [Использование](#usage)
    -   [Создание примера](#building-the-sample)
    -   [Запуск примера](#running-the-sample)
-   [Поддержка](#support)
-   [Минимальные требования](#minimum-requirements)
-   [См. также](#related-topics)

## <a name="usage"></a>Использование

Пример Контекстпопуп можно скачать как автономный проект Microsoft Visual Studio из [центра загрузки Майкрософт](https://www.microsoft.com/DOWNLOADS/en/default.aspx) или установить в составе [пакета средств разработки программного обеспечения (SDK) для Windows](https://msdn.microsoft.com/windows/bb980924.aspx).

-   Центр загрузки Майкрософт: [примеры для ленты Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)
-   Пакет средств разработки программного обеспечения (SDK) для Windows (стандартный путь установки):% ProgramFiles% \\ пакеты SDK Microsoft \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ виндовсриббон \\ контекстпопуп

### <a name="building-the-sample"></a>Построение образца

Загрузите пример на жесткий диск.

Установите Windows SDK для Windows 7 и Откройте командное окно среды сборки. В меню &quot;Пуск&quot; выделите пункты &quot;Все программы&quot;, &quot;Пакет SDK для Microsoft Windows&quot;, а затем &quot;Оболочки CMD&quot;.

Чтобы построить образец из окна командной строки среды построения, перейдите в исходный каталог образца. В командной строке введите команду MSBUILD.

Чтобы построить образец в Microsoft Visual Studio, загрузите решение образца или файл проекта и нажмите сочетание клавиш CTRL + SHIFT + B.

### <a name="running-the-sample"></a>Запуск примера

Чтобы запустить пример из командного окна среды сборки, выполните EXE файлы в \\ папке bin Debug или Bin release, которая \\ содержится в исходной папке Sample.

Для запуска скомпилированного образца с помощью отладки в Visual Studio, нажмите клавишу F5.

## <a name="support"></a>Поддержка

На [форуме по разработке ленты Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) можно обсудить темы и задавать вопросы, связанные с разработкой приложений ленты Windows.

## <a name="minimum-requirements"></a>Минимальные требования



| Требование | Значение |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows 7<br/> Windows Vista с пакетом обновления 2 (SP2) и [обновлением платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Минимальная версия сервера | Windows Server 2008 R2<br/> Windows Server 2008 с пакетом обновления 2 (SP2) и [обновлением платформы для Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Пакет Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Заголовочные и IDL-файлы     | уириббон. h, уириббон. idl                                                                                                                                                 |



 

> [!Note]  
> [Обновление платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) и [обновление платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) — это наборы библиотек времени выполнения, которые позволяют разработчикам ориентироваться на Windows vista и Windows Server 2008 для приложений ленты Windows. Обновления платформы будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows. Сторонние приложения, требующие [обновления платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) или [обновления платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) , могут иметь центр обновления Windows определить, установлена ли требуемая обновленная система. Если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Контекстное всплывающее окно](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





