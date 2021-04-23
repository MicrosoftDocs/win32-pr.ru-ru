---
description: Указывает, записываются ли метаданные в перекодированный файл.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Атрибут MF_TRANSCODE_SKIP_METADATA_TRANSFER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263358"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a><span data-ttu-id="4b7de-103">\_Перекодировать \_ атрибут пропуска \_ метаданных \_</span><span class="sxs-lookup"><span data-stu-id="4b7de-103">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute</span></span>

<span data-ttu-id="4b7de-104">Указывает, записываются ли метаданные в перекодированный файл.</span><span class="sxs-lookup"><span data-stu-id="4b7de-104">Specifies whether metadata is written to the transcoded file.</span></span> <span data-ttu-id="4b7de-105">Этот атрибут контейнера хранится в профиле перекодирования.</span><span class="sxs-lookup"><span data-stu-id="4b7de-105">This container attribute is stored in the transcode profile.</span></span>

## <a name="data-type"></a><span data-ttu-id="4b7de-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4b7de-106">Data type</span></span>

<span data-ttu-id="4b7de-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4b7de-107">**UINT32**</span></span>

<span data-ttu-id="4b7de-108">\_ \_ В следующей таблице описаны возможные значения атрибута, пропуская \_ \_ Перенаправление метаданных MF.</span><span class="sxs-lookup"><span data-stu-id="4b7de-108">Possible values for the MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute are described in the following table.</span></span>



| <span data-ttu-id="4b7de-109">Значение</span><span class="sxs-lookup"><span data-stu-id="4b7de-109">Value</span></span>                                                                        | <span data-ttu-id="4b7de-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4b7de-110">Meaning</span></span>                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b7de-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4b7de-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4b7de-112">Автоматически передает метаданные на уровне файлов из исходного файла в перекодированный файл.</span><span class="sxs-lookup"><span data-stu-id="4b7de-112">Automatically transfers file-level metadata from the source file to the transcoded file.</span></span><br/> |
| <dl> <span data-ttu-id="4b7de-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4b7de-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4b7de-114">Метаданные исходного файла не записываются в перекодированный файл.</span><span class="sxs-lookup"><span data-stu-id="4b7de-114">The source file metadata is not written to the transcoded file.</span></span><br/>                          |



 

## <a name="getset"></a><span data-ttu-id="4b7de-115">Get/Set</span><span class="sxs-lookup"><span data-stu-id="4b7de-115">Get/set</span></span>

<span data-ttu-id="4b7de-116">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4b7de-116">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4b7de-117">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4b7de-117">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b7de-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b7de-118">Remarks</span></span>

<span data-ttu-id="4b7de-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4b7de-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b7de-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4b7de-120">Requirements</span></span>



| <span data-ttu-id="4b7de-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4b7de-121">Requirement</span></span> | <span data-ttu-id="4b7de-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4b7de-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7de-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b7de-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b7de-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4b7de-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b7de-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b7de-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b7de-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b7de-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4b7de-127">Header</span><span class="sxs-lookup"><span data-stu-id="4b7de-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b7de-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b7de-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b7de-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b7de-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b7de-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b7de-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b7de-131">**Имфтранскодепрофиле:: Жетконтаинераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="4b7de-131">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="4b7de-132">**Имфтранскодепрофиле:: Сетконтаинераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="4b7de-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




