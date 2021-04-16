---
description: Возвращает пользовательский значок устройства.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'Метод IWiaUIExtension2:: Жетдевицеикон (Виадевд. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541951"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="35369-103">Метод IWiaUIExtension2:: Жетдевицеикон</span><span class="sxs-lookup"><span data-stu-id="35369-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="35369-104">Возвращает пользовательский значок устройства.</span><span class="sxs-lookup"><span data-stu-id="35369-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="35369-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35369-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="35369-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35369-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35369-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35369-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35369-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35369-108">Type: **BSTR**</span></span>

<span data-ttu-id="35369-109">Указывает идентификатор устройства WIA, для которого должен быть получен значок.</span><span class="sxs-lookup"><span data-stu-id="35369-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="35369-110">*фикон* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35369-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35369-111">Тип: \**Хикон \** _</span><span class="sxs-lookup"><span data-stu-id="35369-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="35369-112">Указывает на место в памяти, которое будет принимать маркер для значка устройства.</span><span class="sxs-lookup"><span data-stu-id="35369-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="35369-113">_nSize \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="35369-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35369-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="35369-114">Type: **ULONG**</span></span>

<span data-ttu-id="35369-115">Задает требуемый размер значка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="35369-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="35369-116">Предполагается, что значок является квадратным, а Нсизе задает ширину и высоту запрошенного значка.</span><span class="sxs-lookup"><span data-stu-id="35369-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35369-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35369-117">Return value</span></span>

<span data-ttu-id="35369-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="35369-118">Type: **HRESULT**</span></span>

<span data-ttu-id="35369-119">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="35369-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="35369-120">Если метод завершается с ошибкой, возвращается соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="35369-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="35369-121">В следующей таблице показаны некоторые из возможных кодов состояния возврата.</span><span class="sxs-lookup"><span data-stu-id="35369-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="35369-122">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="35369-122">Error code</span></span>    | <span data-ttu-id="35369-123">Описание</span><span class="sxs-lookup"><span data-stu-id="35369-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35369-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="35369-124">E\_INVALIDARG</span></span> | <span data-ttu-id="35369-125">Параметр Бстрдевицеид или Фикон имеет **значение NULL**, или бстрдевицеид не указывает на допустимую строку идентификатора устройства WIA</span><span class="sxs-lookup"><span data-stu-id="35369-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="35369-126">\_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="35369-126">E\_FAIL</span></span>       | <span data-ttu-id="35369-127">Нет доступных ресурсов значков.</span><span class="sxs-lookup"><span data-stu-id="35369-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="35369-128">E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="35369-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="35369-129">Не доступен значок требуемого размера.</span><span class="sxs-lookup"><span data-stu-id="35369-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="35369-130">Требования</span><span class="sxs-lookup"><span data-stu-id="35369-130">Requirements</span></span>



| <span data-ttu-id="35369-131">Требование</span><span class="sxs-lookup"><span data-stu-id="35369-131">Requirement</span></span> | <span data-ttu-id="35369-132">Значение</span><span class="sxs-lookup"><span data-stu-id="35369-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35369-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35369-133">Minimum supported client</span></span><br/> | <span data-ttu-id="35369-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="35369-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35369-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35369-135">Minimum supported server</span></span><br/> | <span data-ttu-id="35369-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35369-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35369-137">Header</span><span class="sxs-lookup"><span data-stu-id="35369-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="35369-138"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="35369-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




