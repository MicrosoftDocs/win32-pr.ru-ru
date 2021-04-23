---
description: Создает перечислитель для форматов обмена, которые поддерживает устройство Windows Image (WIA) 2,0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'Метод Ивиатрансфер:: EnumWIA_FORMAT_INFO (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682736"
---
# <a name="iwiatransferenumwia_format_info-method"></a><span data-ttu-id="16381-103">\_Метод сведения о формате ивиатрансфер:: енумвиа \_</span><span class="sxs-lookup"><span data-stu-id="16381-103">IWiaTransfer::EnumWIA\_FORMAT\_INFO method</span></span>

<span data-ttu-id="16381-104">Создает перечислитель для форматов обмена, которые поддерживает устройство Windows Image (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="16381-104">Creates an enumerator for the transfer formats that the Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="16381-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16381-105">Syntax</span></span>


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="16381-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16381-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16381-107">*ппиенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="16381-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16381-108">Тип: **[ **\_ \_ сведения о формате иенумвиа**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="16381-108">Type: **[**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span></span>

<span data-ttu-id="16381-109">Адрес указателя на [**\_ \_ Информационный интерфейс формата иенумвиа**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) для перечислителя.</span><span class="sxs-lookup"><span data-stu-id="16381-109">The address of the pointer to the [**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) interface for the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16381-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16381-110">Return value</span></span>

<span data-ttu-id="16381-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="16381-111">Type: **HRESULT**</span></span>

<span data-ttu-id="16381-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="16381-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16381-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16381-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16381-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16381-114">Remarks</span></span>

<span data-ttu-id="16381-115">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателя интерфейса, полученного через параметр *ппиенум* .</span><span class="sxs-lookup"><span data-stu-id="16381-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointer received through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="16381-116">Требования</span><span class="sxs-lookup"><span data-stu-id="16381-116">Requirements</span></span>



| <span data-ttu-id="16381-117">Требование</span><span class="sxs-lookup"><span data-stu-id="16381-117">Requirement</span></span> | <span data-ttu-id="16381-118">Значение</span><span class="sxs-lookup"><span data-stu-id="16381-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16381-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16381-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16381-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16381-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="16381-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16381-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16381-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16381-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="16381-123">Header</span><span class="sxs-lookup"><span data-stu-id="16381-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="16381-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="16381-124"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="16381-125">IDL</span><span class="sxs-lookup"><span data-stu-id="16381-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="16381-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="16381-126"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="16381-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16381-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="16381-128"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16381-128"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
