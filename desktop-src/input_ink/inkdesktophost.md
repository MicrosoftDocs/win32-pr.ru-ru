---
description: Реализует интерфейс Иинкдесктофост.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Класс Инкдесктофост
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: 74eebdbdfdbe3a4018d63b1f2161687152ebb5cc
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689227"
---
# <a name="inkdesktophost-class"></a><span data-ttu-id="7518d-103">Класс Инкдесктофост</span><span class="sxs-lookup"><span data-stu-id="7518d-103">InkDesktopHost class</span></span>

<span data-ttu-id="7518d-104">Реализует интерфейс [**иинкдесктофост**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .</span><span class="sxs-lookup"><span data-stu-id="7518d-104">Implements the [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) interface.</span></span>

<span data-ttu-id="7518d-105">Объект [**иинкдесктофост**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) обеспечивает рукописный ввод, обработку и отрисовку посредством создания потока приложения для размещения объекта [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) и вставки его в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) приложения.</span><span class="sxs-lookup"><span data-stu-id="7518d-105">An [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) object enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

## <a name="members"></a><span data-ttu-id="7518d-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="7518d-106">Members</span></span>

<span data-ttu-id="7518d-107">Класс **инкдесктофост** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7518d-107">The **InkDesktopHost** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7518d-108">**Инкдесктофост** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7518d-108">**InkDesktopHost** also has these types of members:</span></span>

- [<span data-ttu-id="7518d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="7518d-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7518d-110">Методы</span><span class="sxs-lookup"><span data-stu-id="7518d-110">Methods</span></span>

<span data-ttu-id="7518d-111">Класс **инкдесктофост** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7518d-111">The **InkDesktopHost** class has these methods.</span></span>

| <span data-ttu-id="7518d-112">Метод</span><span class="sxs-lookup"><span data-stu-id="7518d-112">Method</span></span> | <span data-ttu-id="7518d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7518d-113">Description</span></span> |
|---|---|
| [<span data-ttu-id="7518d-114">**креатеандинитиализеинкпресентер**</span><span class="sxs-lookup"><span data-stu-id="7518d-114">**CreateAndInitializeInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | <span data-ttu-id="7518d-115">Создает объект [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) в потоке приложения, подключает его к визуальному дереву [DirectComposition](../directcomp/directcomposition-portal.md) приложения и задает размер объекта.</span><span class="sxs-lookup"><span data-stu-id="7518d-115">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread, connects it to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree, and sets the size of the object.</span></span><br/> |
| [<span data-ttu-id="7518d-116">**креатеинкпресентер**</span><span class="sxs-lookup"><span data-stu-id="7518d-116">**CreateInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | <span data-ttu-id="7518d-117">Создает объект [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) в потоке приложения.</span><span class="sxs-lookup"><span data-stu-id="7518d-117">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread.</span></span><br/> |
| [<span data-ttu-id="7518d-118">**куеуеворкитем**</span><span class="sxs-lookup"><span data-stu-id="7518d-118">**QueueWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | <span data-ttu-id="7518d-119">Добавьте операцию рукописного ввода в рабочую очередь для выполнения в потоке **инкдесктофост** .</span><span class="sxs-lookup"><span data-stu-id="7518d-119">Add an ink operation to a work queue for execution on the **InkDesktopHost** thread.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="7518d-120">\\Функции доступа для создания</span><span class="sxs-lookup"><span data-stu-id="7518d-120">Creation\\Access Functions</span></span>

<span data-ttu-id="7518d-121">Вызовите [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса <strong>инкдесктофост</strong> , чтобы получить ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="7518d-121">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkDesktopHost</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a><span data-ttu-id="7518d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7518d-122">Requirements</span></span>

| <span data-ttu-id="7518d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7518d-123">Requirement</span></span> | <span data-ttu-id="7518d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7518d-124">Value</span></span> |
|---|---|
| <span data-ttu-id="7518d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7518d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7518d-126">Windows 10 \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7518d-126">Windows 10 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7518d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7518d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7518d-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7518d-128">None supported</span></span><br/> |
| <span data-ttu-id="7518d-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7518d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7518d-130"><dt>Инкпресентердесктоп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7518d-130"><dt>InkPresenterDesktop.h</dt></span></span> </dl>   |
| <span data-ttu-id="7518d-131">IDL</span><span class="sxs-lookup"><span data-stu-id="7518d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7518d-132"><dt>Инкпресентердесктоп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7518d-132"><dt>InkPresenterDesktop.idl</dt></span></span> </dl> |
| <span data-ttu-id="7518d-133">IID</span><span class="sxs-lookup"><span data-stu-id="7518d-133">IID</span></span><br/>                      | <span data-ttu-id="7518d-134">IID \_ иинкдесктофост определен как 4ce7d875-a981-4140-a1ff-ad93258e8d59</span><span class="sxs-lookup"><span data-stu-id="7518d-134">IID\_IInkDesktopHost is defined as 4ce7d875-a981-4140-a1ff-ad93258e8d59</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="7518d-135">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="7518d-135">Related topics</span></span>

<span data-ttu-id="7518d-136">[Классы для рукописного ввода](ink-presenter-classes.md), [взаимодействие пером и](/windows/uwp/design/input/pen-and-stylus-interactions)пера, [Пример анализа рукописного ввода](/samples/microsoft/windows-universal-samples/inkanalysis/), [простой пример](/samples/microsoft/windows-universal-samples/simpleink/)с рукописным вводом, [сложный пример для рукописного](/samples/microsoft/windows-universal-samples/complexink/) ввода</span><span class="sxs-lookup"><span data-stu-id="7518d-136">[Ink presenter classes](ink-presenter-classes.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
