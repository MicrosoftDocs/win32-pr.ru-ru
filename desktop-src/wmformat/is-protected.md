---
title: Is_Protected
description: '\_Атрибут protected является атрибутом уровня файла, который указывает, защищено ли содержимое файла с помощью управления цифровыми правами (DRM).'
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected формат Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105710231"
---
# <a name="is_protected"></a><span data-ttu-id="57b7e-104">\_Защищено</span><span class="sxs-lookup"><span data-stu-id="57b7e-104">Is\_Protected</span></span>

<span data-ttu-id="57b7e-105">Атрибут **\_ protected** является атрибутом уровня файла, который указывает, защищено ли содержимое файла с помощью управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="57b7e-105">The **Is\_Protected** attribute is a file-level attribute specifying whether the content in the file was protected using digital rights management (DRM).</span></span>

## <a name="global-constant"></a><span data-ttu-id="57b7e-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="57b7e-106">Global Constant</span></span>

<span data-ttu-id="57b7e-107">g \_ всзвмпротектед</span><span class="sxs-lookup"><span data-stu-id="57b7e-107">g\_wszWMProtected</span></span>

## <a name="data-type"></a><span data-ttu-id="57b7e-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="57b7e-108">Data Type</span></span>

<span data-ttu-id="57b7e-109">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="57b7e-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="57b7e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57b7e-110">Remarks</span></span>

<span data-ttu-id="57b7e-111">Это закодированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="57b7e-111">This is a coded attribute.</span></span> <span data-ttu-id="57b7e-112">Получение этого свойства предоставляет те же сведения, что и вызов [**вмисконтентпротектед**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span><span class="sxs-lookup"><span data-stu-id="57b7e-112">Retrieving this property provides the same information as calling [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span></span>

<span data-ttu-id="57b7e-113">Этот атрибут не может дублироваться на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="57b7e-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="57b7e-114">Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="57b7e-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="57b7e-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57b7e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b7e-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="57b7e-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




