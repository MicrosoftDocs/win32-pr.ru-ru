---
title: Свойство IMsRdpCameraRedirConfigCollection BySymbolicLink
description: Возвращает из коллекции объект Имсрдпкамераредирконфиг, соответствующий заданной символьной ссылке интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Бисимболиклинк
- Службы удаленных рабочих столов свойства Бисимболиклинк, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Бисимболиклинк
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719220"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a><span data-ttu-id="8f461-106">Имсрдпкамераредирконфигколлектион::. Бисимболиклинк, свойство</span><span class="sxs-lookup"><span data-stu-id="8f461-106">IMsRdpCameraRedirConfigCollection::.BySymbolicLink property</span></span>

<span data-ttu-id="8f461-107">Возвращает из коллекции объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданной символьной ссылке интерфейса **KSCATEGORY_VIDEO_CAMERA** для камеры.</span><span class="sxs-lookup"><span data-stu-id="8f461-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="8f461-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8f461-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f461-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f461-109">Syntax</span></span>

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="8f461-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8f461-110">Property value</span></span>

<span data-ttu-id="8f461-111">Объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий указанной символической ссылке.</span><span class="sxs-lookup"><span data-stu-id="8f461-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified symbolic link.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f461-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8f461-112">Requirements</span></span>

| <span data-ttu-id="8f461-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8f461-113">Requirement</span></span> | <span data-ttu-id="8f461-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8f461-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="8f461-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f461-115">Minimum supported client</span></span>| <span data-ttu-id="8f461-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="8f461-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="8f461-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8f461-117">Type library</span></span>            | <span data-ttu-id="8f461-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="8f461-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="8f461-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8f461-119">DLL</span></span>                  | <span data-ttu-id="8f461-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="8f461-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="8f461-121">IID</span><span class="sxs-lookup"><span data-stu-id="8f461-121">IID</span></span>                      | <span data-ttu-id="8f461-122">IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="8f461-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="8f461-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f461-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f461-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="8f461-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>