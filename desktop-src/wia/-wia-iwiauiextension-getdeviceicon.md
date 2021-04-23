---
description: Возвращает пользовательский значок устройства.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Метод Ивиауиекстенсион:: Жетдевицеикон (Виадевд. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145388"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="e6379-103">Метод Ивиауиекстенсион:: Жетдевицеикон</span><span class="sxs-lookup"><span data-stu-id="e6379-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="e6379-104">Возвращает пользовательский значок устройства.</span><span class="sxs-lookup"><span data-stu-id="e6379-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6379-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6379-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="e6379-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6379-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6379-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6379-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6379-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e6379-108">Type: **BSTR**</span></span>

<span data-ttu-id="e6379-109">Указывает идентификатор устройства WIA, для которого должен быть получен значок.</span><span class="sxs-lookup"><span data-stu-id="e6379-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="e6379-110">*фикон* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e6379-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6379-111">Тип: \**Хикон \** _</span><span class="sxs-lookup"><span data-stu-id="e6379-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="e6379-112">Указывает на место в памяти, которое будет принимать маркер для значка устройства.</span><span class="sxs-lookup"><span data-stu-id="e6379-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="e6379-113">_nSize \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e6379-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6379-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="e6379-114">Type: **ULONG**</span></span>

<span data-ttu-id="e6379-115">Задает требуемый размер значка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e6379-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="e6379-116">Предполагается, что значок является квадратным, а Нсизе задает ширину и высоту запрошенного значка.</span><span class="sxs-lookup"><span data-stu-id="e6379-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6379-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6379-117">Return value</span></span>

<span data-ttu-id="e6379-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e6379-118">Type: **HRESULT**</span></span>

<span data-ttu-id="e6379-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e6379-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6379-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6379-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6379-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e6379-121">Requirements</span></span>



| <span data-ttu-id="e6379-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e6379-122">Requirement</span></span> | <span data-ttu-id="e6379-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e6379-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e6379-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6379-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6379-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e6379-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e6379-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6379-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6379-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6379-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e6379-128">Header</span><span class="sxs-lookup"><span data-stu-id="e6379-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6379-129"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6379-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




