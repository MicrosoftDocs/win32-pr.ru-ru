---
title: Свойство IMsRdpCameraRedirConfigCollection ByIndex
description: Возвращает объект Имсрдпкамераредирконфиг по его индексу в коллекции.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Биндекс
- Службы удаленных рабочих столов свойства Биндекс, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Биндекс
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719216"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a><span data-ttu-id="f5a22-106">Свойство Имсрдпкамераредирконфигколлектион:: Биндекс</span><span class="sxs-lookup"><span data-stu-id="f5a22-106">IMsRdpCameraRedirConfigCollection::ByIndex property</span></span>

<span data-ttu-id="f5a22-107">Возвращает объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) по его индексу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="f5a22-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>

<span data-ttu-id="f5a22-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f5a22-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a22-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5a22-109">Syntax</span></span>

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="f5a22-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f5a22-110">Property value</span></span>

<span data-ttu-id="f5a22-111">Объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) , соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="f5a22-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a22-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f5a22-112">Requirements</span></span>

| <span data-ttu-id="f5a22-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f5a22-113">Requirement</span></span> | <span data-ttu-id="f5a22-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f5a22-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f5a22-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5a22-115">Minimum supported client</span></span>| <span data-ttu-id="f5a22-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="f5a22-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f5a22-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f5a22-117">Type library</span></span>            | <span data-ttu-id="f5a22-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f5a22-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f5a22-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f5a22-119">DLL</span></span>                  | <span data-ttu-id="f5a22-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f5a22-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f5a22-121">IID</span><span class="sxs-lookup"><span data-stu-id="f5a22-121">IID</span></span>                      | <span data-ttu-id="f5a22-122">IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="f5a22-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="f5a22-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5a22-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a22-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="f5a22-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>