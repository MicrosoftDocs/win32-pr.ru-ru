---
title: хасаттачедимажес
description: Атрибут Хасаттачедимажес представляет собой атрибут уровня файла, указывающий, является ли файл MP3-файлом с подключенными кадрами APIC ID3.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Формат Windows Media Хасаттачедимажес
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691448"
---
# <a name="hasattachedimages"></a><span data-ttu-id="4641c-104">хасаттачедимажес</span><span class="sxs-lookup"><span data-stu-id="4641c-104">HasAttachedImages</span></span>

<span data-ttu-id="4641c-105">Атрибут **хасаттачедимажес** представляет собой атрибут уровня файла, указывающий, является ли файл MP3-файлом с подключенными КАДРАМИ APIC ID3.</span><span class="sxs-lookup"><span data-stu-id="4641c-105">The **HasAttachedImages** attribute is a file-level attribute specifying whether the file is an MP3 file with attached APIC ID3 frames.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4641c-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="4641c-106">Global Constant</span></span>

<span data-ttu-id="4641c-107">g \_ всзвмхасаттачедимажес</span><span class="sxs-lookup"><span data-stu-id="4641c-107">g\_wszWMHasAttachedImages</span></span>

## <a name="data-type"></a><span data-ttu-id="4641c-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4641c-108">Data Type</span></span>

<span data-ttu-id="4641c-109">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="4641c-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="4641c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4641c-110">Remarks</span></span>

<span data-ttu-id="4641c-111">Это закодированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="4641c-111">This is a coded attribute.</span></span>

<span data-ttu-id="4641c-112">Этот атрибут не может дублироваться на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="4641c-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="4641c-113">Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4641c-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="4641c-114">**Хасаттачедимажес** был разработан для информирования приложения о наличии изображений, чтобы их можно было получить с помощью интерфейса [**ивмимажеинфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) .</span><span class="sxs-lookup"><span data-stu-id="4641c-114">**HasAttachedImages** was designed to inform an application that images were present so that they could be retrieved using the [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) interface.</span></span> <span data-ttu-id="4641c-115">Теперь, когда образы поддерживаются с помощью атрибута [**WM/Picture**](wmpicture.md) , **хасаттачедимажес** больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="4641c-115">Now that images are supported using the [**WM/Picture**](wmpicture.md) attribute, **HasAttachedImages** is no longer needed.</span></span>

<span data-ttu-id="4641c-116">Чтобы определить, содержит ли файл изображения, вызовите [**IWMHeaderInfo3:: жетаттрибутеиндицес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) , указав атрибут **WM/Picture** .</span><span class="sxs-lookup"><span data-stu-id="4641c-116">To determine whether a file contains images, call [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specifying the **WM/Picture** attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="4641c-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4641c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4641c-118">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="4641c-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




