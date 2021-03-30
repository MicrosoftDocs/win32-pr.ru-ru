---
title: Signature_Name
description: '\_Атрибут имени подписи содержит имя сертификата, используемого для подписания файла. Этот атрибут допустим только в том случае, если \_ атрибуту является Trusted задано значение true.'
ms.assetid: 3f3ab10c-731b-4075-8f73-3c2e62e010b9
keywords:
- Signature_Name формат Windows Media
topic_type:
- apiref
api_name:
- Signature_Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af378671a570dd9ffc58021081b3925d3dca21af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784020"
---
# <a name="signature_name"></a><span data-ttu-id="de778-105">\_Имя подписи</span><span class="sxs-lookup"><span data-stu-id="de778-105">Signature\_Name</span></span>

<span data-ttu-id="de778-106">Атрибут **\_ имени подписи** содержит имя сертификата, используемого для подписания файла.</span><span class="sxs-lookup"><span data-stu-id="de778-106">The **Signature\_Name** attribute contains the name on the certificate used to sign the file.</span></span> <span data-ttu-id="de778-107">Этот атрибут допустим только в том случае, если атрибуту [**является \_ Trusted**](is-trusted.md) задано значение true.</span><span class="sxs-lookup"><span data-stu-id="de778-107">This attribute is valid only if the [**Is\_Trusted**](is-trusted.md) attribute is set to True.</span></span>

## <a name="global-constant"></a><span data-ttu-id="de778-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="de778-108">Global Constant</span></span>

<span data-ttu-id="de778-109">\_всзвмсигнатуре \_ имя</span><span class="sxs-lookup"><span data-stu-id="de778-109">g\_wszWMSignature\_Name</span></span>

## <a name="data-type"></a><span data-ttu-id="de778-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="de778-110">Data Type</span></span>

<span data-ttu-id="de778-111">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="de778-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="de778-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de778-112">Remarks</span></span>

<span data-ttu-id="de778-113">Это закодированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="de778-113">This is a coded attribute.</span></span>

<span data-ttu-id="de778-114">Этот атрибут не может дублироваться на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="de778-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="de778-115">Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="de778-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="de778-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de778-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de778-117">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="de778-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




