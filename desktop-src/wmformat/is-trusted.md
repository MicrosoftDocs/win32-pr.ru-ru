---
title: Is_Trusted
description: Атрибут является \_ доверенным атрибутом уровня файла, который указывает, является ли URL-адрес для получения лицензий в файле доверенным.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted формат Windows Media
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103987024"
---
# <a name="is_trusted"></a><span data-ttu-id="690eb-104">Является \_ доверенным</span><span class="sxs-lookup"><span data-stu-id="690eb-104">Is\_Trusted</span></span>

<span data-ttu-id="690eb-105">Атрибут **является \_ доверенным** атрибутом уровня файла, который указывает, является ли URL-адрес для получения лицензий в файле доверенным.</span><span class="sxs-lookup"><span data-stu-id="690eb-105">The **Is\_Trusted** attribute is a file-level attribute specifying whether the license acquisition URL in the file is trusted.</span></span>

## <a name="global-constant"></a><span data-ttu-id="690eb-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="690eb-106">Global Constant</span></span>

<span data-ttu-id="690eb-107">g \_ всзвмтрустед</span><span class="sxs-lookup"><span data-stu-id="690eb-107">g\_wszWMTrusted</span></span>

## <a name="data-type"></a><span data-ttu-id="690eb-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="690eb-108">Data Type</span></span>

<span data-ttu-id="690eb-109">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="690eb-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="690eb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="690eb-110">Remarks</span></span>

<span data-ttu-id="690eb-111">Это закодированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="690eb-111">This is a coded attribute.</span></span>

<span data-ttu-id="690eb-112">Перед переходом к URL-адресу получения лицензии, содержащемуся в файле, защищенном DRM, приложение должно сначала проверить, имеет ли это свойство значение true.</span><span class="sxs-lookup"><span data-stu-id="690eb-112">Before navigating to a license acquisition URL contained in a DRM-protected file, an application should first verify that this property is true.</span></span> <span data-ttu-id="690eb-113">Если значение равно false, приложение должно уведомлять пользователя о том, что URL-адрес, возможно, был незаконным.</span><span class="sxs-lookup"><span data-stu-id="690eb-113">If it is false, the application should notify the user that the URL has possibly been tampered with.</span></span>

<span data-ttu-id="690eb-114">Этот атрибут не может дублироваться на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="690eb-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="690eb-115">Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="690eb-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="690eb-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="690eb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="690eb-117">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="690eb-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




