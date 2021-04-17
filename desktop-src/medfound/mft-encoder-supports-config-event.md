---
description: Указывает, что кодировщик MFT поддерживает получение событий Минкодингпараметер во время потоковой передачи.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: Атрибут MFT_ENCODER_SUPPORTS_CONFIG_EVENT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656589"
---
# <a name="mft_encoder_supports_config_event-attribute"></a><span data-ttu-id="99414-103">\_КОДИРОВЩИК MFT \_ поддерживает \_ \_ атрибут события конфигурации</span><span class="sxs-lookup"><span data-stu-id="99414-103">MFT\_ENCODER\_SUPPORTS\_CONFIG\_EVENT attribute</span></span>

<span data-ttu-id="99414-104">Указывает, что кодировщик MFT поддерживает получение событий [минкодингпараметер](meencodingparameters.md) во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="99414-104">Specifies that the MFT encoder supports receiving [MEEncodingParameter](meencodingparameters.md) events while streaming.</span></span>

## <a name="data-type"></a><span data-ttu-id="99414-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="99414-105">Data type</span></span>

<span data-ttu-id="99414-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="99414-106">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="99414-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99414-107">Remarks</span></span>

<span data-ttu-id="99414-108">Отправляется кодировщиком MFT через [**имфтрансформ::P роцессевент**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="99414-108">Sent by the MFT encoder through [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="99414-109">Требования</span><span class="sxs-lookup"><span data-stu-id="99414-109">Requirements</span></span>



| <span data-ttu-id="99414-110">Требование</span><span class="sxs-lookup"><span data-stu-id="99414-110">Requirement</span></span> | <span data-ttu-id="99414-111">Значение</span><span class="sxs-lookup"><span data-stu-id="99414-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="99414-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99414-112">Minimum supported client</span></span><br/> | <span data-ttu-id="99414-113">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="99414-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="99414-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99414-114">Minimum supported server</span></span><br/> | <span data-ttu-id="99414-115">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="99414-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="99414-116">Header</span><span class="sxs-lookup"><span data-stu-id="99414-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="99414-117"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="99414-117"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="99414-118">IDL</span><span class="sxs-lookup"><span data-stu-id="99414-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99414-119"><dt>Мфтрансформ. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99414-119"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99414-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99414-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99414-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="99414-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="99414-122">**Имфтрансформ::P Роцессевент**</span><span class="sxs-lookup"><span data-stu-id="99414-122">**IMFTransform::ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




