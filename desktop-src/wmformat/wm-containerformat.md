---
title: WM/Контаинерформат
description: Атрибут WM/Контаинерформат указывает тип файла, который загружается в вызывающий объект.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Формат Windows Media WM/Контаинерформат
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784128"
---
# <a name="wmcontainerformat"></a><span data-ttu-id="df15f-104">WM/Контаинерформат</span><span class="sxs-lookup"><span data-stu-id="df15f-104">WM/ContainerFormat</span></span>

<span data-ttu-id="df15f-105">Атрибут **WM/контаинерформат** указывает тип файла, который загружается в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="df15f-105">The **WM/ContainerFormat** attribute specifies the type of file that is loaded in the calling object.</span></span>

## <a name="global-constant"></a><span data-ttu-id="df15f-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="df15f-106">Global Constant</span></span>

<span data-ttu-id="df15f-107">g \_ всзвмконтаинерформат</span><span class="sxs-lookup"><span data-stu-id="df15f-107">g\_wszWMContainerFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="df15f-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="df15f-108">Data Type</span></span>

<span data-ttu-id="df15f-109">[**ВМТ \_ \_Формат хранения**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**\_ \_ двоичный тип ВМТ**)</span><span class="sxs-lookup"><span data-stu-id="df15f-109">[**WMT\_STORAGE\_FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="df15f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df15f-110">Remarks</span></span>

<span data-ttu-id="df15f-111">Этот атрибут используется вместо **IWMProfile3:: жетсторажеформат** и **IWMProfile3:: сетсторажеформат**, которые больше не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="df15f-111">This attribute is used in place of **IWMProfile3::GetStorageFormat** and **IWMProfile3::SetStorageFormat**, which are no longer supported.</span></span>

<span data-ttu-id="df15f-112">Это закодированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="df15f-112">This is a coded attribute.</span></span>

<span data-ttu-id="df15f-113">Этот атрибут не может дублироваться на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="df15f-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="df15f-114">Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="df15f-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="df15f-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df15f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df15f-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="df15f-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




