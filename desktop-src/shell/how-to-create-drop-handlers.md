---
description: Как реализовать и зарегистрировать обработчик перетаскивания.
title: Создание обработчиков Drop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34c06aa3eae1892b5b86ce3a0f3b1198be41cd2f9dda5c9bd0956b40a53146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223588"
---
# <a name="how-to-create-drop-handlers"></a>Создание обработчиков Drop

По умолчанию файлы не удаляются. Можно сделать элементы [типа файлов](fa-file-types.md) в целевые объекты перетаскивания путем реализации и регистрации *обработчика перетаскивания*.

Если обработчик перетаскивания зарегистрирован для типа файла, он вызывается всякий раз, когда объект перетаскивается или удаляется для элемента типа файла. Оболочка управляет операцией, вызывая соответствующие методы в интерфейсе [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) обработчика.

Общие процедуры для реализации и регистрации обработчика расширений оболочки обсуждаются в разделе [Создание обработчиков расширений оболочки](handlers.md). В этом документе рассматриваются аспекты реализации, характерные для удаления обработчиков.

## <a name="instructions"></a>Инструкции

### <a name="step-1-implementing-drop-handlers"></a>Шаг 1. Реализация обработчиков Drop

Как и все обработчики расширений оболочки, обработчики Drop — это объекты модели COM, реализованные в виде библиотек DLL. В дополнение к [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) и [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget), они экспортируют два интерфейса.

Оболочка инициализирует обработчик с помощью своего интерфейса [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Он использует этот интерфейс для запроса идентификатора класса (CLSID) обработчика и предоставляет ему имя файла. Общее описание способов реализации обработчиков расширений оболочки, включая интерфейс **IPersistFile** , см. в разделе [Создание обработчиков расширений оболочки](handlers.md).

После инициализации обработчика удаления оболочка вызывает соответствующий метод в интерфейсе [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) обработчика.

### <a name="step-2-registering-drop-handlers"></a>Шаг 2. Регистрация обработчиков перетаскивания

Обработчики удаления регистрируются в подразделе этого типа файла.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Создайте подраздел **дрофандлер** с именем для обработчика и задайте в качестве значения по умолчанию для подраздела строку GUID CLSID обработчика. Общие сведения о регистрации обработчиков расширений оболочки см. в статье [Создание обработчиков расширений](handlers.md)оболочки.

В следующем примере показаны записи реестра, которые включают обработчик перетаскивания для типа файла example. МИП.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание обработчиков расширений оболочки](handlers.md)
</dt> <dt>

[**Интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
