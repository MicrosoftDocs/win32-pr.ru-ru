---
description: Интерфейс ITablet3 позволяет Мультисенсорная запросы входных данных.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Интерфейс ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712814"
---
# <a name="itablet3-interface"></a><span data-ttu-id="dc9c8-103">Интерфейс ITablet3</span><span class="sxs-lookup"><span data-stu-id="dc9c8-103">ITablet3 interface</span></span>

<span data-ttu-id="dc9c8-104">Интерфейс ITablet3 позволяет Мультисенсорная запросы входных данных.</span><span class="sxs-lookup"><span data-stu-id="dc9c8-104">The ITablet3 interface enables multitouch querying for input.</span></span>

## <a name="members"></a><span data-ttu-id="dc9c8-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="dc9c8-105">Members</span></span>

<span data-ttu-id="dc9c8-106">Интерфейс **ITablet3** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dc9c8-106">The **ITablet3** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc9c8-107">**ITablet3** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc9c8-107">**ITablet3** also has these types of members:</span></span>

-   [<span data-ttu-id="dc9c8-108">Методы</span><span class="sxs-lookup"><span data-stu-id="dc9c8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc9c8-109">Методы</span><span class="sxs-lookup"><span data-stu-id="dc9c8-109">Methods</span></span>

<span data-ttu-id="dc9c8-110">Интерфейс **ITablet3** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dc9c8-110">The **ITablet3** interface has these methods.</span></span>



| <span data-ttu-id="dc9c8-111">Метод</span><span class="sxs-lookup"><span data-stu-id="dc9c8-111">Method</span></span>                                                  | <span data-ttu-id="dc9c8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dc9c8-112">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="dc9c8-113">**жетмаксимумкурсорс**</span><span class="sxs-lookup"><span data-stu-id="dc9c8-113">**GetMaximumCursors**</span></span>](itablet3-getmaximumcursors.md) | <span data-ttu-id="dc9c8-114">Возвращает максимальное число поддерживаемых входных данных.</span><span class="sxs-lookup"><span data-stu-id="dc9c8-114">Retrieves the maximum number of inputs supported.</span></span><br/>        |
| [<span data-ttu-id="dc9c8-115">**исмултитауч**</span><span class="sxs-lookup"><span data-stu-id="dc9c8-115">**isMultiTouch**</span></span>](itablet3-ismultitouch.md)           | <span data-ttu-id="dc9c8-116">Указывает, включен ли Мультисенсорная для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="dc9c8-116">Indicates whether multitouch is enabled for this object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc9c8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc9c8-117">Remarks</span></span>

<span data-ttu-id="dc9c8-118">Разработчики не должны использовать этот интерфейс</span><span class="sxs-lookup"><span data-stu-id="dc9c8-118">Developers should not use this interface</span></span>

<span data-ttu-id="dc9c8-119">В следующем коде показано, как определяется интерфейс **ITablet3** .</span><span class="sxs-lookup"><span data-stu-id="dc9c8-119">The following code describes how the **ITablet3** interface is defined.</span></span>

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a><span data-ttu-id="dc9c8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dc9c8-120">Requirements</span></span>



| <span data-ttu-id="dc9c8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dc9c8-121">Requirement</span></span> | <span data-ttu-id="dc9c8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dc9c8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9c8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc9c8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9c8-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dc9c8-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dc9c8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc9c8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9c8-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc9c8-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dc9c8-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc9c8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc9c8-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc9c8-128"><dt>Wisptis.exe</dt></span></span> </dl> |



 

