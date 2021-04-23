---
title: Свойство IMsRdpCameraRedirConfigCollection RedirectByDefault
description: Указывает, будет ли перенаправлена какая либо новая камера по умолчанию.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректбидефаулт
- Службы удаленных рабочих столов свойства Редиректбидефаулт, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Редиректбидефаулт
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104139175"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a><span data-ttu-id="00a65-106">Свойство Имсрдпкамераредирконфигколлектион:: Редиректбидефаулт</span><span class="sxs-lookup"><span data-stu-id="00a65-106">IMsRdpCameraRedirConfigCollection::RedirectByDefault property</span></span>

<span data-ttu-id="00a65-107">Указывает, будет ли перенаправлена какая либо новая камера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="00a65-107">Specifies whether or not any new camera gets redirected by default.</span></span>

<span data-ttu-id="00a65-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="00a65-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a65-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00a65-109">Syntax</span></span>

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a><span data-ttu-id="00a65-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="00a65-110">Property value</span></span>

<span data-ttu-id="00a65-111">Значение, указывающее, перенаправляется ли новая камера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="00a65-111">A value that indicates whether or not any new camera gets redirected by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="00a65-112">Требования</span><span class="sxs-lookup"><span data-stu-id="00a65-112">Requirements</span></span>

| <span data-ttu-id="00a65-113">Требование</span><span class="sxs-lookup"><span data-stu-id="00a65-113">Requirement</span></span> | <span data-ttu-id="00a65-114">Значение</span><span class="sxs-lookup"><span data-stu-id="00a65-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="00a65-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00a65-115">Minimum supported client</span></span>| <span data-ttu-id="00a65-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="00a65-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="00a65-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="00a65-117">Type library</span></span>            | <span data-ttu-id="00a65-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="00a65-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="00a65-119">DLL</span><span class="sxs-lookup"><span data-stu-id="00a65-119">DLL</span></span>                  | <span data-ttu-id="00a65-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="00a65-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="00a65-121">IID</span><span class="sxs-lookup"><span data-stu-id="00a65-121">IID</span></span>                      | <span data-ttu-id="00a65-122">IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="00a65-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="00a65-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00a65-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a65-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="00a65-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>