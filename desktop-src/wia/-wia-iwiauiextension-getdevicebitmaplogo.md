---
description: Возвращает пользовательский логотип точечного рисунка для устройства.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'Метод Ивиауиекстенсион:: Жетдевицебитмаплого (Виадевд. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692422"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a><span data-ttu-id="6ab7c-103">Метод Ивиауиекстенсион:: Жетдевицебитмаплого</span><span class="sxs-lookup"><span data-stu-id="6ab7c-103">IWiaUIExtension::GetDeviceBitmapLogo method</span></span>

<span data-ttu-id="6ab7c-104">Возвращает пользовательский логотип точечного рисунка для устройства.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-104">Gets a custom bitmap logo for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab7c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ab7c-105">Syntax</span></span>


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a><span data-ttu-id="6ab7c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ab7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab7c-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ab7c-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab7c-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6ab7c-108">Type: **BSTR**</span></span>

<span data-ttu-id="6ab7c-109">Указывает идентификатор устройства WIA, для которого должен быть получен значок.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="6ab7c-110">*фбитмап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6ab7c-110">*phBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab7c-111">Тип: \**хбитмап \** _</span><span class="sxs-lookup"><span data-stu-id="6ab7c-111">Type: \**HBITMAP\** _</span></span>

<span data-ttu-id="6ab7c-112">Указывает на место в памяти, которое будет принимать маркер эмблемы точечного рисунка для устройства.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-112">Points to a memory location that will receive a handle for the bitmap logo for the device.</span></span>

</dd> <dt>

<span data-ttu-id="6ab7c-113">_nMaxWidth \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6ab7c-113">_nMaxWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab7c-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="6ab7c-114">Type: **ULONG**</span></span>

<span data-ttu-id="6ab7c-115">Задает желаемую ширину точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-115">Specifies the desired width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="6ab7c-116">*нмаксхеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ab7c-116">*nMaxHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab7c-117">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="6ab7c-117">Type: **ULONG**</span></span>

<span data-ttu-id="6ab7c-118">Задает желаемую высоту точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-118">Specifies the desired height of the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab7c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ab7c-119">Return value</span></span>

<span data-ttu-id="6ab7c-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6ab7c-120">Type: **HRESULT**</span></span>

<span data-ttu-id="6ab7c-121">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ab7c-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ab7c-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab7c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6ab7c-123">Requirements</span></span>



| <span data-ttu-id="6ab7c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6ab7c-124">Requirement</span></span> | <span data-ttu-id="6ab7c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6ab7c-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab7c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ab7c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab7c-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ab7c-127">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6ab7c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ab7c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab7c-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ab7c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6ab7c-130">Header</span><span class="sxs-lookup"><span data-stu-id="6ab7c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab7c-131"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ab7c-131"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




