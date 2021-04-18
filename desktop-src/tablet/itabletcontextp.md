---
description: Представляет контекст планшета.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Интерфейс Итаблетконтекстп
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713063"
---
# <a name="itabletcontextp-interface"></a><span data-ttu-id="4df03-103">Интерфейс Итаблетконтекстп</span><span class="sxs-lookup"><span data-stu-id="4df03-103">ITabletContextP interface</span></span>

<span data-ttu-id="4df03-104">Представляет контекст планшета.</span><span class="sxs-lookup"><span data-stu-id="4df03-104">Represents the tablet context.</span></span>

## <a name="members"></a><span data-ttu-id="4df03-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="4df03-105">Members</span></span>

<span data-ttu-id="4df03-106">Интерфейс **итаблетконтекстп** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4df03-106">The **ITabletContextP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4df03-107">**Итаблетконтекстп** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4df03-107">**ITabletContextP** also has these types of members:</span></span>

-   [<span data-ttu-id="4df03-108">Методы</span><span class="sxs-lookup"><span data-stu-id="4df03-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4df03-109">Методы</span><span class="sxs-lookup"><span data-stu-id="4df03-109">Methods</span></span>

<span data-ttu-id="4df03-110">Интерфейс **итаблетконтекстп** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4df03-110">The **ITabletContextP** interface has these methods.</span></span>



| <span data-ttu-id="4df03-111">Метод</span><span class="sxs-lookup"><span data-stu-id="4df03-111">Method</span></span>                                                                                           | <span data-ttu-id="4df03-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4df03-112">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="4df03-113">**истопмоссук**</span><span class="sxs-lookup"><span data-stu-id="4df03-113">**IsTopMostHook**</span></span>](itabletcontextp-istopmosthook.md)                                           | <span data-ttu-id="4df03-114">Указывает, находится ли контекст планшета в самом верхнем обработчике.</span><span class="sxs-lookup"><span data-stu-id="4df03-114">Indicates if the tablet context is in the top most hook.</span></span><br/>             |
| [<span data-ttu-id="4df03-115">**Перекрытие**</span><span class="sxs-lookup"><span data-stu-id="4df03-115">**Overlap**</span></span>](itabletcontextp-overlap.md)                                                       | <span data-ttu-id="4df03-116">Перемещает контекст планшета на передний или задний план входной очереди.</span><span class="sxs-lookup"><span data-stu-id="4df03-116">Moves a tablet context to the front or back of the input queue.</span></span><br/>      |
| [<span data-ttu-id="4df03-117">**траккинпутрект**</span><span class="sxs-lookup"><span data-stu-id="4df03-117">**TrackInputRect**</span></span>](itabletcontextp-trackinputrect.md)                                         | <span data-ttu-id="4df03-118">Обновляет планшет дигитайзер до координат сопоставления расположения окна.</span><span class="sxs-lookup"><span data-stu-id="4df03-118">Updates the tablet digitizer to window location mapping coordinates.</span></span><br/> |
| [<span data-ttu-id="4df03-119">**усенамедшаредмеморикоммуникатионс**</span><span class="sxs-lookup"><span data-stu-id="4df03-119">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md) | <span data-ttu-id="4df03-120">Предоставляет доступ к памяти, используемой между потоками планшета.</span><span class="sxs-lookup"><span data-stu-id="4df03-120">Provides access to memory shared between tablet threads.</span></span><br/>             |
| [<span data-ttu-id="4df03-121">**усешаредмеморикоммуникатионс**</span><span class="sxs-lookup"><span data-stu-id="4df03-121">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)           | <span data-ttu-id="4df03-122">Предоставляет доступ к памяти, используемой между потоками планшета.</span><span class="sxs-lookup"><span data-stu-id="4df03-122">Provides access to memory shared between tablet threads.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="4df03-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4df03-123">Remarks</span></span>

<span data-ttu-id="4df03-124">Разработчики не должны использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4df03-124">Developers should not use this interface.</span></span>

<span data-ttu-id="4df03-125">[**Усенамедшаредмеморикоммуникатионс**](itabletcontextp-usenamedsharedmemorycommunications.md) доступен только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="4df03-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) is only available on Windows Vista and later.</span></span>

<span data-ttu-id="4df03-126">В следующем коде показано, как определяется интерфейс **итаблетконтекстп** .</span><span class="sxs-lookup"><span data-stu-id="4df03-126">The following code describes how the **ITabletContextP** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a><span data-ttu-id="4df03-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4df03-127">Requirements</span></span>



| <span data-ttu-id="4df03-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4df03-128">Requirement</span></span> | <span data-ttu-id="4df03-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4df03-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df03-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4df03-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4df03-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4df03-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4df03-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4df03-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4df03-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4df03-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4df03-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4df03-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="4df03-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4df03-135"><dt>Wisptis.exe</dt></span></span> </dl> |



 

