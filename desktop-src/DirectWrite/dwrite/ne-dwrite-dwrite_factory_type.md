---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Указывает тип объекта фабрики DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 87b0d1c2edcb836afd06d732f242b62441b9bd01
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881813"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="8582f-103">Перечисление DWRITE_FACTORY_TYPE (дврите. h)</span><span class="sxs-lookup"><span data-stu-id="8582f-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="8582f-104">Указывает тип объекта фабрики DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="8582f-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8582f-105">Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="8582f-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="8582f-106">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="8582f-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="8582f-107">Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="8582f-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="8582f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8582f-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a><span data-ttu-id="8582f-109">Константы</span><span class="sxs-lookup"><span data-stu-id="8582f-109">Constants</span></span>

| <span data-ttu-id="8582f-110">Имя</span><span class="sxs-lookup"><span data-stu-id="8582f-110">Name</span></span> | <span data-ttu-id="8582f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8582f-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="8582f-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="8582f-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="8582f-113">Указывает, что фабрика DirectWrite является общей фабрикой и позволяет повторно использовать кэшированные данные шрифтов в нескольких компонентах внутри процесса.</span><span class="sxs-lookup"><span data-stu-id="8582f-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="8582f-114">Такие фабрики также используют компоненты кэширования шрифтов между процессами для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="8582f-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="8582f-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="8582f-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="8582f-116">Указывает, что объект фабрики DirectWrite является изолированным.</span><span class="sxs-lookup"><span data-stu-id="8582f-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="8582f-117">Объекты, созданные из изолированной фабрики, не взаимодействуют с внутренним состоянием DirectWrite из других компонентов.</span><span class="sxs-lookup"><span data-stu-id="8582f-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="8582f-118">DWRITE_FACTORY_TYPE_ISOLATED2</span><span class="sxs-lookup"><span data-stu-id="8582f-118">DWRITE_FACTORY_TYPE_ISOLATED2</span></span> | <span data-ttu-id="8582f-119">Указывает, что объект фабрики DirectWrite ограничен.</span><span class="sxs-lookup"><span data-stu-id="8582f-119">Indicates that the DirectWrite factory object is restricted.</span></span> <span data-ttu-id="8582f-120">Объекты, созданные из ограниченной фабрики, не используют и не изменяют внутреннее состояние или кэшированные данные, используемые другими фабриками.</span><span class="sxs-lookup"><span data-stu-id="8582f-120">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="8582f-121">Кроме того, системная коллекция шрифтов содержит только хорошо известные шрифты.</span><span class="sxs-lookup"><span data-stu-id="8582f-121">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="8582f-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="8582f-122">Examples</span></span>

<span data-ttu-id="8582f-123">См. раздел [Обзор двритекоре](/windows/win32/DirectWrite/dwrite/dwritecore-overview) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="8582f-123">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="8582f-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="8582f-124">Remarks</span></span>

<span data-ttu-id="8582f-125">Объект фабрики DirectWrite содержит сведения о его внутреннем состоянии, такие как регистрация загрузчика шрифтов и кэшированные данные шрифта.</span><span class="sxs-lookup"><span data-stu-id="8582f-125">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="8582f-126">В большинстве случаев следует использовать объект Shared Factory, так как он позволяет нескольким компонентам, использующим DirectWrite, обмениваться внутренними сведениями о состоянии DirectWrite, тем самым уменьшая использование памяти.</span><span class="sxs-lookup"><span data-stu-id="8582f-126">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="8582f-127">Однако бывают случаи, когда желательно уменьшить воздействие компонента на остальную часть процесса, например подключаемый модуль из ненадежного источника, с помощью песочницы и изоляции его от остальных компонентов процесса.</span><span class="sxs-lookup"><span data-stu-id="8582f-127">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="8582f-128">В таких случаях для изолированного компонента следует использовать изолированную фабрику.</span><span class="sxs-lookup"><span data-stu-id="8582f-128">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="8582f-129">Ограниченная фабрика больше заблокирована, чем изолированная фабрика.</span><span class="sxs-lookup"><span data-stu-id="8582f-129">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="8582f-130">Он не взаимодействует с межпроцессным или постоянным кэшем шрифтов каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="8582f-130">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="8582f-131">Кроме того, системная коллекция шрифтов, возвращаемая из этой фабрики, включает только хорошо известные шрифты.</span><span class="sxs-lookup"><span data-stu-id="8582f-131">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="8582f-132">При передаче **DWRITE_FACTORY_TYPE_ISOLATED2** в более раннюю версию дврите, чем Двритекоре, [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) возвращает **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="8582f-132">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8582f-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8582f-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8582f-134">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="8582f-134">**Minimum supported client**</span></span> | <span data-ttu-id="8582f-135">Windows 10, переобъединение проектов [приложения Win32]</span><span class="sxs-lookup"><span data-stu-id="8582f-135">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="8582f-136">**Header**</span><span class="sxs-lookup"><span data-stu-id="8582f-136">**Header**</span></span> | <span data-ttu-id="8582f-137">дврите. h (включает dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="8582f-137">dwrite.h (include dwrite_core.h)</span></span> |
