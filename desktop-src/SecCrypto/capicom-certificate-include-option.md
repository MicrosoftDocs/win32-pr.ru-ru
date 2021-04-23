---
description: Определяет, какие сертификаты в цепочке сохраняются.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Перечисление CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668803"
---
# <a name="capicom_certificate_include_option-enumeration"></a><span data-ttu-id="39147-103">\_ \_ Перечисление параметров для включения CAPICOM Certificate \_</span><span class="sxs-lookup"><span data-stu-id="39147-103">CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION enumeration</span></span>

<span data-ttu-id="39147-104">Тип **перечисления \_ "CAPICOM Certificate \_ include \_ "** определяет, какие сертификаты в цепочке сохраняются.</span><span class="sxs-lookup"><span data-stu-id="39147-104">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type defines which certificates in a chain are saved.</span></span> <span data-ttu-id="39147-105">Этот тип перечисления появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="39147-105">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="39147-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="39147-106">Members</span></span>



| <span data-ttu-id="39147-107">Член</span><span class="sxs-lookup"><span data-stu-id="39147-107">Member</span></span>                                                 | <span data-ttu-id="39147-108">Описание</span><span class="sxs-lookup"><span data-stu-id="39147-108">Description</span></span>                                                                           | <span data-ttu-id="39147-109">Значение</span><span class="sxs-lookup"><span data-stu-id="39147-109">Value</span></span> |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="39147-110">**CAPICOM \_ Certificate \_ включает \_ цепочку, \_ кроме \_ root**</span><span class="sxs-lookup"><span data-stu-id="39147-110">**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</span></span> | <span data-ttu-id="39147-111">Сохраняет все сертификаты в цепочке, за исключением корневой сущности.</span><span class="sxs-lookup"><span data-stu-id="39147-111">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> | <span data-ttu-id="39147-112">0</span><span class="sxs-lookup"><span data-stu-id="39147-112">0</span></span>     |
| <span data-ttu-id="39147-113">**CAPICOM \_ Certificate \_ включает \_ всю \_ цепочку**</span><span class="sxs-lookup"><span data-stu-id="39147-113">**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</span></span>        | <span data-ttu-id="39147-114">Сохраняет всю цепочку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="39147-114">Saves the complete certificate chain.</span></span><br/>                                      | <span data-ttu-id="39147-115">1</span><span class="sxs-lookup"><span data-stu-id="39147-115">1</span></span>     |
| <span data-ttu-id="39147-116">**CAPICOM \_ Certificate \_ — \_ только конечная \_ сущность \_**</span><span class="sxs-lookup"><span data-stu-id="39147-116">**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</span></span>   | <span data-ttu-id="39147-117">Сохраняет только сертификат конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="39147-117">Saves only the end entity certificate.</span></span><br/>                                     | <span data-ttu-id="39147-118">2</span><span class="sxs-lookup"><span data-stu-id="39147-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="39147-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39147-119">Remarks</span></span>

<span data-ttu-id="39147-120">Тип **перечисления \_ \_ \_ "CAPICOM Certificate include** " используется методом [**Certificate. Save**](certificate-save.md) .</span><span class="sxs-lookup"><span data-stu-id="39147-120">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="39147-121">Требования</span><span class="sxs-lookup"><span data-stu-id="39147-121">Requirements</span></span>



| <span data-ttu-id="39147-122">Требование</span><span class="sxs-lookup"><span data-stu-id="39147-122">Requirement</span></span> | <span data-ttu-id="39147-123">Значение</span><span class="sxs-lookup"><span data-stu-id="39147-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39147-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="39147-124">Redistributable</span></span><br/> | <span data-ttu-id="39147-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="39147-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="39147-126">Header</span><span class="sxs-lookup"><span data-stu-id="39147-126">Header</span></span><br/>          | <dl> <span data-ttu-id="39147-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="39147-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




