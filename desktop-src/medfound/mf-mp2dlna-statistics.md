---
description: Возвращает статистику для приемника мультимедиа Digital живая Network Alliance (DLNA).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: Атрибут MF_MP2DLNA_STATISTICS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544367"
---
# <a name="mf_mp2dlna_statistics-attribute"></a><span data-ttu-id="65034-103">\_ \_ Атрибут статистики MF MP2DLNA</span><span class="sxs-lookup"><span data-stu-id="65034-103">MF\_MP2DLNA\_STATISTICS attribute</span></span>

<span data-ttu-id="65034-104">Возвращает статистику для приемника мультимедиа Digital живая Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="65034-104">Gets statistics from the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="65034-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="65034-105">Data type</span></span>

<span data-ttu-id="65034-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** хранится в **виде \[ \] байта**</span><span class="sxs-lookup"><span data-stu-id="65034-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="65034-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="65034-107">Get/set</span></span>

<span data-ttu-id="65034-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="65034-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="65034-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65034-109">Remarks</span></span>

<span data-ttu-id="65034-110">Во время потоковой передачи приемник мультимедиа DLNA обновляет этот атрибут со статистикой о кодировке и мультиплексировании потоков MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="65034-110">During streaming, the DLNA media sink updates this attribute with statistics about the encoding and multiplexing of the MPEG-2 streams.</span></span> <span data-ttu-id="65034-111">Приложение может в любое время запросить этот атрибут для получения последних значений.</span><span class="sxs-lookup"><span data-stu-id="65034-111">The application can query this attribute at any time to get the latest values.</span></span>

<span data-ttu-id="65034-112">Установка этого атрибута для приемника мультимедиа DLNA не оказывает никакого воздействия.</span><span class="sxs-lookup"><span data-stu-id="65034-112">Setting this attribute on the DLNA media sink has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="65034-113">Требования</span><span class="sxs-lookup"><span data-stu-id="65034-113">Requirements</span></span>



| <span data-ttu-id="65034-114">Требование</span><span class="sxs-lookup"><span data-stu-id="65034-114">Requirement</span></span> | <span data-ttu-id="65034-115">Значение</span><span class="sxs-lookup"><span data-stu-id="65034-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65034-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65034-116">Minimum supported client</span></span><br/> | <span data-ttu-id="65034-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="65034-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="65034-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65034-118">Minimum supported server</span></span><br/> | <span data-ttu-id="65034-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="65034-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="65034-120">Header</span><span class="sxs-lookup"><span data-stu-id="65034-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="65034-121"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="65034-121"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65034-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65034-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65034-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="65034-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




