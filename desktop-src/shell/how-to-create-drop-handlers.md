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
# <a name="how-to-create-drop-handlers"></a><span data-ttu-id="dd957-103">Создание обработчиков Drop</span><span class="sxs-lookup"><span data-stu-id="dd957-103">How to Create Drop Handlers</span></span>

<span data-ttu-id="dd957-104">По умолчанию файлы не удаляются.</span><span class="sxs-lookup"><span data-stu-id="dd957-104">By default, files are not drop targets.</span></span> <span data-ttu-id="dd957-105">Можно сделать элементы [типа файлов](fa-file-types.md) в целевые объекты перетаскивания путем реализации и регистрации *обработчика перетаскивания*.</span><span class="sxs-lookup"><span data-stu-id="dd957-105">You can make the members of a [file type](fa-file-types.md) into drop targets by implementing and registering a *drop handler*.</span></span>

<span data-ttu-id="dd957-106">Если обработчик перетаскивания зарегистрирован для типа файла, он вызывается всякий раз, когда объект перетаскивается или удаляется для элемента типа файла.</span><span class="sxs-lookup"><span data-stu-id="dd957-106">If a drop handler is registered for a file type, it is called whenever an object is dragged over or dropped on a member of the file type.</span></span> <span data-ttu-id="dd957-107">Оболочка управляет операцией, вызывая соответствующие методы в интерфейсе [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) обработчика.</span><span class="sxs-lookup"><span data-stu-id="dd957-107">The Shell manages the operation by calling the appropriate methods on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

<span data-ttu-id="dd957-108">Общие процедуры для реализации и регистрации обработчика расширений оболочки обсуждаются в разделе [Создание обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="dd957-108">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="dd957-109">В этом документе рассматриваются аспекты реализации, характерные для удаления обработчиков.</span><span class="sxs-lookup"><span data-stu-id="dd957-109">This document focuses on those aspects of implementation that are specific to drop handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="dd957-110">Инструкции</span><span class="sxs-lookup"><span data-stu-id="dd957-110">Instructions</span></span>

### <a name="step-1-implementing-drop-handlers"></a><span data-ttu-id="dd957-111">Шаг 1. Реализация обработчиков Drop</span><span class="sxs-lookup"><span data-stu-id="dd957-111">Step 1: Implementing Drop Handlers</span></span>

<span data-ttu-id="dd957-112">Как и все обработчики расширений оболочки, обработчики Drop — это объекты модели COM, реализованные в виде библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="dd957-112">Like all Shell extension handlers, drop handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="dd957-113">В дополнение к [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) и [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget), они экспортируют два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dd957-113">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span></span>

<span data-ttu-id="dd957-114">Оболочка инициализирует обработчик с помощью своего интерфейса [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="dd957-114">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="dd957-115">Он использует этот интерфейс для запроса идентификатора класса (CLSID) обработчика и предоставляет ему имя файла.</span><span class="sxs-lookup"><span data-stu-id="dd957-115">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="dd957-116">Общее описание способов реализации обработчиков расширений оболочки, включая интерфейс **IPersistFile** , см. в разделе [Создание обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="dd957-116">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="dd957-117">После инициализации обработчика удаления оболочка вызывает соответствующий метод в интерфейсе [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) обработчика.</span><span class="sxs-lookup"><span data-stu-id="dd957-117">Once the drop handler is initialized, the Shell calls the appropriate method on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

### <a name="step-2-registering-drop-handlers"></a><span data-ttu-id="dd957-118">Шаг 2. Регистрация обработчиков перетаскивания</span><span class="sxs-lookup"><span data-stu-id="dd957-118">Step 2: Registering Drop Handlers</span></span>

<span data-ttu-id="dd957-119">Обработчики удаления регистрируются в подразделе этого типа файла.</span><span class="sxs-lookup"><span data-stu-id="dd957-119">Drop handlers are registered under this file type's subkey.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

<span data-ttu-id="dd957-120">Создайте подраздел **дрофандлер** с именем для обработчика и задайте в качестве значения по умолчанию для подраздела строку GUID CLSID обработчика.</span><span class="sxs-lookup"><span data-stu-id="dd957-120">Create a subkey of **DropHandler** named for the handler, and set the subkey's default value to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="dd957-121">Общие сведения о регистрации обработчиков расширений оболочки см. в статье [Создание обработчиков расширений](handlers.md)оболочки.</span><span class="sxs-lookup"><span data-stu-id="dd957-121">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="dd957-122">В следующем примере показаны записи реестра, которые включают обработчик перетаскивания для типа файла example. МИП.</span><span class="sxs-lookup"><span data-stu-id="dd957-122">The following example illustrates registry entries that enable a drop handler for an example .myp file type.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="dd957-123">См. также</span><span class="sxs-lookup"><span data-stu-id="dd957-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd957-124">Создание обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="dd957-124">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="dd957-125">**Интерфейс IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="dd957-125">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[<span data-ttu-id="dd957-126">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="dd957-126">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
