---
title: Свойство IMsRdpCameraRedirConfigCollection ByInstanceId
description: Возвращает из коллекции объект Имсрдпкамераредирконфиг, соответствующий заданному ИДЕНТИФИКАТОРу экземпляра.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Бинстанцеид
- Службы удаленных рабочих столов свойства Бинстанцеид, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Бинстанцеид
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494148"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a><span data-ttu-id="209c7-106">Свойство Имсрдпкамераредирконфигколлектион:: Бинстанцеид</span><span class="sxs-lookup"><span data-stu-id="209c7-106">IMsRdpCameraRedirConfigCollection::ByInstanceId property</span></span>

<span data-ttu-id="209c7-107">Возвращает из коллекции объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданному идентификатору экземпляра.</span><span class="sxs-lookup"><span data-stu-id="209c7-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>

<span data-ttu-id="209c7-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="209c7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="209c7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="209c7-109">Syntax</span></span>

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="209c7-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="209c7-110">Property value</span></span>

<span data-ttu-id="209c7-111">Объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий заданному идентификатору экземпляра.</span><span class="sxs-lookup"><span data-stu-id="209c7-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified instance ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="209c7-112">Требования</span><span class="sxs-lookup"><span data-stu-id="209c7-112">Requirements</span></span>

| <span data-ttu-id="209c7-113">Требование</span><span class="sxs-lookup"><span data-stu-id="209c7-113">Requirement</span></span> | <span data-ttu-id="209c7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="209c7-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="209c7-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="209c7-115">Minimum supported client</span></span>| <span data-ttu-id="209c7-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="209c7-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="209c7-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="209c7-117">Type library</span></span>            | <span data-ttu-id="209c7-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="209c7-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="209c7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="209c7-119">DLL</span></span>                  | <span data-ttu-id="209c7-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="209c7-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="209c7-121">IID</span><span class="sxs-lookup"><span data-stu-id="209c7-121">IID</span></span>                      | <span data-ttu-id="209c7-122">IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="209c7-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="209c7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="209c7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209c7-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="209c7-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>