---
description: 'Метод Ивиауиекстенсион:: Жетдевицеикон — получает значок настраиваемого устройства.'
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
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116662"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="75060-103">Метод Ивиауиекстенсион:: Жетдевицеикон</span><span class="sxs-lookup"><span data-stu-id="75060-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="75060-104">Возвращает пользовательский значок устройства.</span><span class="sxs-lookup"><span data-stu-id="75060-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="75060-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75060-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="75060-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75060-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75060-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75060-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75060-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="75060-108">Type: **BSTR**</span></span>

<span data-ttu-id="75060-109">Указывает идентификатор устройства WIA, для которого должен быть получен значок.</span><span class="sxs-lookup"><span data-stu-id="75060-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="75060-110">*фикон* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75060-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75060-111">Тип: **Хикон \***</span><span class="sxs-lookup"><span data-stu-id="75060-111">Type: **HICON\***</span></span>

<span data-ttu-id="75060-112">Указывает на место в памяти, которое будет принимать маркер для значка устройства.</span><span class="sxs-lookup"><span data-stu-id="75060-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="75060-113">*нсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75060-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75060-114">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="75060-114">Type: **ULONG**</span></span>

<span data-ttu-id="75060-115">Задает требуемый размер значка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="75060-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="75060-116">Предполагается, что значок является квадратным, а Нсизе задает ширину и высоту запрошенного значка.</span><span class="sxs-lookup"><span data-stu-id="75060-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75060-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75060-117">Return value</span></span>

<span data-ttu-id="75060-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="75060-118">Type: **HRESULT**</span></span>

<span data-ttu-id="75060-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="75060-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75060-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75060-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="75060-121">Требования</span><span class="sxs-lookup"><span data-stu-id="75060-121">Requirements</span></span>



| <span data-ttu-id="75060-122">Требование</span><span class="sxs-lookup"><span data-stu-id="75060-122">Requirement</span></span> | <span data-ttu-id="75060-123">Значение</span><span class="sxs-lookup"><span data-stu-id="75060-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75060-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75060-124">Minimum supported client</span></span><br/> | <span data-ttu-id="75060-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="75060-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="75060-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75060-126">Minimum supported server</span></span><br/> | <span data-ttu-id="75060-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75060-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75060-128">Header</span><span class="sxs-lookup"><span data-stu-id="75060-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="75060-129"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="75060-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




