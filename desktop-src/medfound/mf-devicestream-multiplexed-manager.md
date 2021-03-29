---
description: Предоставляет экземпляр Имфмуксстреаматтрибутесманажер, который управляет Имфаттрибутес, описывающим подпотоки мультиплексированного источника мультимедиа.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Атрибут MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647240"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a><span data-ttu-id="9c637-103">\_Атрибут девицестреам \_ мультиплексированного \_ диспетчера MF</span><span class="sxs-lookup"><span data-stu-id="9c637-103">MF\_DEVICESTREAM\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="9c637-104">Предоставляет экземпляр [**имфмуксстреаматтрибутесманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) , который управляет [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , описывающим подпотоки мультиплексированного источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9c637-104">Provides an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) which manages the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) describing the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="9c637-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9c637-105">Data type</span></span>

<span data-ttu-id="9c637-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="9c637-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="9c637-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c637-107">Remarks</span></span>

<span data-ttu-id="9c637-108">Передайте это значение в [**имфаттрибутес:: Ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) , чтобы определить, предоставляет ли источник мультимедиа мультиплексированные потоки, и, если это так, получите экземпляр [**имфмуксстреаматтрибутесманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span><span class="sxs-lookup"><span data-stu-id="9c637-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to determine if the media source provides multiplexed streams and, if so, get an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c637-109">Требования</span><span class="sxs-lookup"><span data-stu-id="9c637-109">Requirements</span></span>



| <span data-ttu-id="9c637-110">Требование</span><span class="sxs-lookup"><span data-stu-id="9c637-110">Requirement</span></span> | <span data-ttu-id="9c637-111">Значение</span><span class="sxs-lookup"><span data-stu-id="9c637-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c637-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c637-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9c637-113">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="9c637-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9c637-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c637-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9c637-115">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9c637-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="9c637-116">Header</span><span class="sxs-lookup"><span data-stu-id="9c637-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c637-117"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c637-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
