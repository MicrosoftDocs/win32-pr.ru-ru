---
description: Указывает, поддерживает ли преобразование Media Foundation (MFT) Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: Атрибут MF_SA_D3D11_AWARE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344175"
---
# <a name="mf_sa_d3d11_aware-attribute"></a><span data-ttu-id="c3727-103">\_Атрибут MF SA \_ D3D11 с \_ поддержкой</span><span class="sxs-lookup"><span data-stu-id="c3727-103">MF\_SA\_D3D11\_AWARE attribute</span></span>

<span data-ttu-id="c3727-104">Указывает, поддерживает ли преобразование Media Foundation (MFT) Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="c3727-104">Specifies whether a Media Foundation transform (MFT) supports Microsoft Direct3D 11.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3727-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c3727-105">Data type</span></span>

<span data-ttu-id="c3727-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c3727-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c3727-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3727-107">Remarks</span></span>

<span data-ttu-id="c3727-108">Этот атрибут применяется только к видео МФТС.</span><span class="sxs-lookup"><span data-stu-id="c3727-108">This attribute applies only to video MFTs.</span></span> <span data-ttu-id="c3727-109">Чтобы запросить этот атрибут, вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить хранилище атрибутов MFT.</span><span class="sxs-lookup"><span data-stu-id="c3727-109">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT attribute store.</span></span> <span data-ttu-id="c3727-110">Если методы **InAttribute** выполнены, вызовите [**ИМФАТТРИБУТЕС:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c3727-110">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

-   <span data-ttu-id="c3727-111">Если атрибут не равен нулю, клиент может предоставить MFT указатель на интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) перед запуском потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="c3727-111">If the attribute is nonzero, the client can give the MFT a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface before streaming starts.</span></span> <span data-ttu-id="c3727-112">Для этого клиент отправляет в основную таблицу сообщений [**MFT \_ сообщение \_ \_ \_ диспетчера D3D**](mft-message-set-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="c3727-112">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="c3727-113">Клиенту не требуется отсылать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="c3727-113">The client is not required to send this message.</span></span>
-   <span data-ttu-id="c3727-114">Если этот атрибут равен нулю (**false**), то MFT не поддерживает Direct3D 11, и клиент не должен отсылать сообщение [**MFT \_ \_ \_ \_ диспетчера D3D**](mft-message-set-d3d-manager.md) в основную таблицу файлов.</span><span class="sxs-lookup"><span data-stu-id="c3727-114">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 11, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="c3727-115">Значение этого атрибута по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="c3727-115">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="c3727-116">Рассматривайте этот атрибут как доступный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c3727-116">Treat this attribute as read-only.</span></span> <span data-ttu-id="c3727-117">Не изменяйте значение. в MFT все изменения в значении будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="c3727-117">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3727-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c3727-118">Requirements</span></span>



| <span data-ttu-id="c3727-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c3727-119">Requirement</span></span> | <span data-ttu-id="c3727-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c3727-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3727-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3727-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c3727-122">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c3727-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c3727-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3727-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c3727-124">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c3727-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c3727-125">Header</span><span class="sxs-lookup"><span data-stu-id="c3727-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3727-126"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3727-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3727-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3727-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3727-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3727-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3727-129">Поддержка декодирования видео Direct3D 11 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3727-129">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




