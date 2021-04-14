---
description: Расширение буфера обмена с помощью пользовательских обработчиков формата данных.
title: Создание обработчиков данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997710"
---
# <a name="how-to-create-data-handlers"></a><span data-ttu-id="91f98-103">Создание обработчиков данных</span><span class="sxs-lookup"><span data-stu-id="91f98-103">How to Create Data Handlers</span></span>

<span data-ttu-id="91f98-104">Когда файл копируется в буфер обмена или перетаскивается и удаляется, оболочка создает объект данных, поддерживающий разнообразные стандартные [форматы буфера обмена](dragdrop.md).</span><span class="sxs-lookup"><span data-stu-id="91f98-104">When a file is copied to the clipboard or dragged and dropped, the Shell creates a data object that supports a variety of standard [clipboard formats](dragdrop.md).</span></span> <span data-ttu-id="91f98-105">Для файлов определенного типа можно расширить доступные форматы буфера обмена, реализовав и зарегистрировав *обработчик данных*.</span><span class="sxs-lookup"><span data-stu-id="91f98-105">For files that are of a specific file type, you can extend the available clipboard formats by implementing and registering a *data handler*.</span></span> <span data-ttu-id="91f98-106">При передаче файла типа файла оболочка делегирует вызовы интерфейса [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) объекта данных обработчику данных, если используется один из пользовательских форматов.</span><span class="sxs-lookup"><span data-stu-id="91f98-106">When a file of the file type is transferred, the Shell delegates calls to the data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface to the data handler if one of the custom formats is used.</span></span>

<span data-ttu-id="91f98-107">Общие процедуры для реализации и регистрации обработчика расширений оболочки обсуждаются в разделе [Создание обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="91f98-107">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="91f98-108">В этом документе рассматриваются аспекты реализации, характерные для обработчиков данных.</span><span class="sxs-lookup"><span data-stu-id="91f98-108">This document focuses on those aspects of implementation that are specific to data handlers.</span></span>

-   [<span data-ttu-id="91f98-109">Реализация обработчиков данных</span><span class="sxs-lookup"><span data-stu-id="91f98-109">Implementing Data Handlers</span></span>](#step-1-implementing-data-handlers)
-   [<span data-ttu-id="91f98-110">Регистрация обработчиков данных</span><span class="sxs-lookup"><span data-stu-id="91f98-110">Registering Data Handlers</span></span>](#step-2-registering-data-handlers)
-   [<span data-ttu-id="91f98-111">См. также</span><span class="sxs-lookup"><span data-stu-id="91f98-111">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="91f98-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="91f98-112">Instructions</span></span>

### <a name="step-1-implementing-data-handlers"></a><span data-ttu-id="91f98-113">Шаг 1. Реализация обработчиков данных</span><span class="sxs-lookup"><span data-stu-id="91f98-113">Step 1: Implementing Data Handlers</span></span>

<span data-ttu-id="91f98-114">Как и все обработчики расширений оболочки, обработчики данных — это объекты модели COM, реализованные в виде библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="91f98-114">Like all Shell extension handlers, data handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="91f98-115">Они экспортируют два интерфейса в дополнение к [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) и [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="91f98-115">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span></span>

<span data-ttu-id="91f98-116">Оболочка инициализирует обработчик с помощью своего интерфейса [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="91f98-116">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="91f98-117">Он использует этот интерфейс для запроса идентификатора класса (CLSID) обработчика и предоставляет ему имя файла.</span><span class="sxs-lookup"><span data-stu-id="91f98-117">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="91f98-118">Общее описание способов реализации обработчиков расширений оболочки, включая интерфейс **IPersistFile** , см. в разделе [Создание обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="91f98-118">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="91f98-119">После инициализации обработчика данных оболочка делегирует вызовы из объекта данных интерфейсу [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) обработчика, если используется один из пользовательских форматов.</span><span class="sxs-lookup"><span data-stu-id="91f98-119">Once the data handler is initialized, the Shell delegates calls from the data object to the handler's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface if one of the custom formats is used.</span></span>

### <a name="step-2-registering-data-handlers"></a><span data-ttu-id="91f98-120">Шаг 2. Регистрация обработчиков данных</span><span class="sxs-lookup"><span data-stu-id="91f98-120">Step 2: Registering Data Handlers</span></span>

<span data-ttu-id="91f98-121">Обработчики данных регистрируются в подразделе *ProgID* типа файла, как показано ниже **: \_ классы hKey \_ root** \\ *ProgID* \\ **шеллекс** данных \\ **дескриптора**</span><span class="sxs-lookup"><span data-stu-id="91f98-121">Data handlers are registered under the file type's *ProgID* subkey as shown here: **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shellex**\\**DataHandler**</span></span>

<span data-ttu-id="91f98-122">Создайте подключ с именем для обработчика в разделе " **дескриптор** данных" и задайте значение по умолчанию для подраздела этого обработчика в виде строки GUID идентификатора CLSID обработчика.</span><span class="sxs-lookup"><span data-stu-id="91f98-122">Create a subkey named for the handler under **DataHandler** and set the default value of that handler's subkey to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="91f98-123">Общие сведения о регистрации обработчиков расширений оболочки см. в статье [Создание обработчиков расширений](handlers.md)оболочки.</span><span class="sxs-lookup"><span data-stu-id="91f98-123">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="91f98-124">В следующем примере показаны записи реестра, которые включают обработчик данных для типа файла example. МИП.</span><span class="sxs-lookup"><span data-stu-id="91f98-124">The following example illustrates registry entries that enable a data handler for an example .myp file type.</span></span>

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="91f98-125">См. также</span><span class="sxs-lookup"><span data-stu-id="91f98-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91f98-126">Создание обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="91f98-126">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="91f98-127">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="91f98-127">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[<span data-ttu-id="91f98-128">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="91f98-128">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
