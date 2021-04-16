---
title: Метод IMsRdpCameraRedirConfigCollection AddConfig
description: Добавляет объект Имсрдпкамераредирконфиг в коллекцию (соответствующая камера не должна быть подключена).
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддконфиг
- Службы удаленных рабочих столов метода Аддконфиг, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, метод Аддконфиг
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536380"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a><span data-ttu-id="5cddb-106">Метод Имсрдпкамераредирконфигколлектион:: Аддконфиг</span><span class="sxs-lookup"><span data-stu-id="5cddb-106">IMsRdpCameraRedirConfigCollection::AddConfig method</span></span>

<span data-ttu-id="5cddb-107">Добавляет объект [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) в коллекцию (соответствующая камера не должна быть подключена).</span><span class="sxs-lookup"><span data-stu-id="5cddb-107">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>

## <a name="syntax"></a><span data-ttu-id="5cddb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cddb-108">Syntax</span></span>

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a><span data-ttu-id="5cddb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cddb-109">Parameters</span></span>

<span data-ttu-id="5cddb-110">*symbolicLink* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5cddb-110">*symbolicLink* \[in\]</span></span>

<span data-ttu-id="5cddb-111">Символьная ссылка для нового объекта [имсрдпкамераредирконфиг](imsrdpcameraredirconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="5cddb-111">The symbolic link for the new [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object.</span></span>

<span data-ttu-id="5cddb-112">*фредиректед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5cddb-112">*fRedirected* \[in\]</span></span>

<span data-ttu-id="5cddb-113">Указывает, будет ли перенаправлена новая камера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5cddb-113">Specifies whether or not the new camera gets redirected by default.</span></span>

## <a name="return-value"></a><span data-ttu-id="5cddb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5cddb-114">Return value</span></span>

<span data-ttu-id="5cddb-115">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="5cddb-115">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cddb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5cddb-116">Requirements</span></span>

| <span data-ttu-id="5cddb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5cddb-117">Requirement</span></span> | <span data-ttu-id="5cddb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5cddb-118">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="5cddb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cddb-119">Minimum supported client</span></span>| <span data-ttu-id="5cddb-120">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="5cddb-120">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="5cddb-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5cddb-121">Type library</span></span>            | <span data-ttu-id="5cddb-122">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="5cddb-122">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="5cddb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5cddb-123">DLL</span></span>                  | <span data-ttu-id="5cddb-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="5cddb-124">MsTscAx.dll</span></span>     |
| <span data-ttu-id="5cddb-125">IID</span><span class="sxs-lookup"><span data-stu-id="5cddb-125">IID</span></span>                      | <span data-ttu-id="5cddb-126">IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="5cddb-126">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="5cddb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cddb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cddb-128">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="5cddb-128">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>