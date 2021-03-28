---
description: Как реализовать и зарегистрировать обработчик перетаскивания.
title: Создание обработчиков Drop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264423"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание обработчиков расширений оболочки](handlers.md)
</dt> <dt>

[**Интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
