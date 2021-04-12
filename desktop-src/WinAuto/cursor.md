---
title: Cursor (Справочник по элементам пользовательского интерфейса MSAA)
description: Курсор представляет собой небольшое изображение, положение которого на экране управляется указывающим устройством, например мышью, пером или трекболом. Когда пользователь перемещает указывающее устройство, операционная система Windows перемещает курсор.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328851"
---
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (Справочник по элементам пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются курсоры в целях справочника по элементам пользовательского интерфейса MSAA. Использование курсоров в различных платформах пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Курсор представляет собой небольшое изображение, положение которого на экране управляется указывающим устройством, например мышью, пером или трекболом. Когда пользователь перемещает указывающее устройство, операционная система Windows перемещает курсор.

## <a name="iaccessible-methods"></a>Методы IAccessible

Курсор поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Свойства IAccessible

Курсор поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**Get \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— свойство **ChildCount** равно нулю.
-   [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— разработчики могут создавать пользовательские курсоры или использовать стандартные курсоры, ОПРЕДЕЛЯЕМые по идентификатору курсора. Свойство **Name** курсора зависит от его формы и является одним из следующих: 

    | Форма курсора     | Имя              |
    |------------------|-------------------|
    | Пользовательский курсор    | Неизвестный         |
    | \_стрелка IDC       | "Normal"          |
    | \_ИБЕАМ IDC       | Редактор            |
    | \_Ожидание IDC        | Ожидания            |
    | \_перекрестный IDC       | Графических         |
    | СТРЕЛКА для IDC \_     | Крывающемся              |
    | \_СИЗЕНВСЕ IDC    | "НВСЕ size"       |
    | \_СИЗЕНЕСВ IDC    | "НЕСВ size"       |
    | \_СИЗЕВЕ IDC      | "Размер по горизонтали" |
    | \_СИЗЕНС IDC      | "Размер по вертикали"   |
    | \_СИЗЕАЛЛ IDC     | Поместить            |
    | IDC \_ No          | Запрещено       |
    | \_АППСТАРТИНГ IDC | "Запуск приложения"       |
    | \_Справка по IDC        | Позволяют            |

    

     

-   [**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— свойство **Role** является [**\_ системным \_ курсором роли**](object-roles.md).
-   [**Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— свойство **State** является сочетанием одного или нескольких из следующих [значений](object-state-constants.md):

    [**Состояние \_ Системная \_ невидимая**](object-state-constants.md) \| [ **\_ Система состояний \_ с плавающей запятой**](object-state-constants.md)

## <a name="notes"></a>Примечания

-   В отличие от других элементов пользовательского интерфейса, объект Cursor не имеет связанного с ним маркера окна. Чтобы получить доступ к объекту Cursor, клиенты должны задать [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) и подождать, пока объект курсора не выдаст события.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




