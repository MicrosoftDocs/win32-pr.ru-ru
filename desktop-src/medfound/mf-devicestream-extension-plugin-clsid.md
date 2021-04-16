---
description: Указывает идентификатор CLSID подключаемого модуля последующей обработки для устройства видеозаписи.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: Атрибут MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692508"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a><span data-ttu-id="55066-103">\_ \_ \_ Атрибут CLSID подключаемого модуля расширения девицестреам MF \_</span><span class="sxs-lookup"><span data-stu-id="55066-103">MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute</span></span>

<span data-ttu-id="55066-104">Указывает идентификатор CLSID подключаемого модуля последующей обработки для устройства видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="55066-104">Specifies the CLSID of a post-processing plug-in for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="55066-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="55066-105">Data type</span></span>

<span data-ttu-id="55066-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="55066-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="55066-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55066-107">Remarks</span></span>

<span data-ttu-id="55066-108">Подключаемый модуль последующей обработки — это файл MFT, который обрабатывает видеоизображение после его записи.</span><span class="sxs-lookup"><span data-stu-id="55066-108">A post-processing plug-in is an MFT that processes the video image after it is captured.</span></span> <span data-ttu-id="55066-109">Поставщик оборудования может включать подключаемый модуль последующей обработки в составе установочного пакета.</span><span class="sxs-lookup"><span data-stu-id="55066-109">The hardware vendor can include a post-processing plug-in as part of the installation package.</span></span> <span data-ttu-id="55066-110">Если это так, источник видеозаписи устанавливает \_ \_ \_ атрибут CLSID подключаемого модуля расширения MF девицестреам \_ в идентификатор CLSID подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="55066-110">If so, the video capture source sets the MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute to the CLSID of the plug-in.</span></span>

<span data-ttu-id="55066-111">Чтобы получить этот атрибут, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="55066-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="55066-112">Запросите источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="55066-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="55066-113">Вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для потока.</span><span class="sxs-lookup"><span data-stu-id="55066-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="55066-114">Вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) InAttribute, чтобы получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="55066-114">Call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) to get the attribute.</span></span>

<span data-ttu-id="55066-115">Чтобы создать подключаемый модуль, вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="55066-115">To create the plug-in, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="requirements"></a><span data-ttu-id="55066-116">Требования</span><span class="sxs-lookup"><span data-stu-id="55066-116">Requirements</span></span>



| <span data-ttu-id="55066-117">Требование</span><span class="sxs-lookup"><span data-stu-id="55066-117">Requirement</span></span> | <span data-ttu-id="55066-118">Значение</span><span class="sxs-lookup"><span data-stu-id="55066-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55066-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55066-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55066-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="55066-120">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55066-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55066-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55066-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="55066-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="55066-123">Header</span><span class="sxs-lookup"><span data-stu-id="55066-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55066-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="55066-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55066-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55066-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55066-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55066-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
