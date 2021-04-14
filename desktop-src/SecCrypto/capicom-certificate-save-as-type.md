---
description: Определяет формат файла, содержащего сведения о сертификате.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Перечисление CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668525"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a><span data-ttu-id="50efa-103">\_ \_ \_ \_ Перечисление типа файла CAPICOM Certificate</span><span class="sxs-lookup"><span data-stu-id="50efa-103">CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="50efa-104">Тип перечисления **CAPICOM \_ Certificate \_ resave \_ As \_** определяет формат файла, содержащего сведения о сертификате.</span><span class="sxs-lookup"><span data-stu-id="50efa-104">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificate information.</span></span> <span data-ttu-id="50efa-105">Этот тип перечисления появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="50efa-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="50efa-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="50efa-106">Members</span></span>



| <span data-ttu-id="50efa-107">Член</span><span class="sxs-lookup"><span data-stu-id="50efa-107">Member</span></span>                                  | <span data-ttu-id="50efa-108">Описание</span><span class="sxs-lookup"><span data-stu-id="50efa-108">Description</span></span>                                                                                                                                   | <span data-ttu-id="50efa-109">Значение</span><span class="sxs-lookup"><span data-stu-id="50efa-109">Value</span></span> |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="50efa-110">**CAPICOM \_ Certificate \_ Save \_ как \_ PFX**</span><span class="sxs-lookup"><span data-stu-id="50efa-110">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</span></span> | <span data-ttu-id="50efa-111">Выходной файл будет отформатирован как файл PFX (PKCS 12), а все связанные с ним закрытые ключи также будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="50efa-111">The output file will be formatted as a PFX (PKCS 12) file and any associated private keys which are exportable will also be saved.</span></span><br/> | <span data-ttu-id="50efa-112">0</span><span class="sxs-lookup"><span data-stu-id="50efa-112">0</span></span>     |
| <span data-ttu-id="50efa-113">**CAPICOM \_ Certificate \_ Save \_ как \_ CER**</span><span class="sxs-lookup"><span data-stu-id="50efa-113">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</span></span> | <span data-ttu-id="50efa-114">Выходной файл будет отформатирован как CER-файл без сохранения закрытых ключей.</span><span class="sxs-lookup"><span data-stu-id="50efa-114">The output file will be formatted as a CER file with no private keys saved.</span></span><br/>                                                        | <span data-ttu-id="50efa-115">1</span><span class="sxs-lookup"><span data-stu-id="50efa-115">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="50efa-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50efa-116">Remarks</span></span>

<span data-ttu-id="50efa-117">Тип перечисления **CAPICOM \_ Certificate- \_ \_ \_ Type** используется методом [**Certificate. Save**](certificate-save.md) .</span><span class="sxs-lookup"><span data-stu-id="50efa-117">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50efa-118">Требования</span><span class="sxs-lookup"><span data-stu-id="50efa-118">Requirements</span></span>



| <span data-ttu-id="50efa-119">Требование</span><span class="sxs-lookup"><span data-stu-id="50efa-119">Requirement</span></span> | <span data-ttu-id="50efa-120">Значение</span><span class="sxs-lookup"><span data-stu-id="50efa-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50efa-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="50efa-121">Redistributable</span></span><br/> | <span data-ttu-id="50efa-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="50efa-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="50efa-123">Header</span><span class="sxs-lookup"><span data-stu-id="50efa-123">Header</span></span><br/>          | <dl> <span data-ttu-id="50efa-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="50efa-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




