---
description: Определяет формат файла, содержащего сведения о сертификатах.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Перечисление CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668524"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a><span data-ttu-id="8594c-103">CAPICOM \_ Certificates \_ Сохранить \_ как \_ Перечисление типов</span><span class="sxs-lookup"><span data-stu-id="8594c-103">CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="8594c-104">Тип перечисления **CAPICOM \_ Certificates \_ Save \_ As \_ Type** определяет формат файла, содержащего сведения о сертификатах.</span><span class="sxs-lookup"><span data-stu-id="8594c-104">The **CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificates information.</span></span> <span data-ttu-id="8594c-105">Этот тип перечисления появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="8594c-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="8594c-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="8594c-106">Members</span></span>



| <span data-ttu-id="8594c-107">Член</span><span class="sxs-lookup"><span data-stu-id="8594c-107">Member</span></span>                                          | <span data-ttu-id="8594c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8594c-108">Description</span></span>                                          | <span data-ttu-id="8594c-109">Значение</span><span class="sxs-lookup"><span data-stu-id="8594c-109">Value</span></span> |
|-------------------------------------------------|------------------------------------------------------|-------|
| <span data-ttu-id="8594c-110">**CAPICOM \_ Certificates \_ Сохранить \_ как \_ сериализованный**</span><span class="sxs-lookup"><span data-stu-id="8594c-110">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</span></span> | <span data-ttu-id="8594c-111">Сохраненные сертификаты сериализуются.</span><span class="sxs-lookup"><span data-stu-id="8594c-111">The saved certificates are serialized.</span></span><br/>    | <span data-ttu-id="8594c-112">0</span><span class="sxs-lookup"><span data-stu-id="8594c-112">0</span></span>     |
| <span data-ttu-id="8594c-113">**CAPICOM \_ Certificates \_ Сохранить \_ как \_ PKCS7**</span><span class="sxs-lookup"><span data-stu-id="8594c-113">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</span></span>      | <span data-ttu-id="8594c-114">Сертификаты сохраняются в виде PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="8594c-114">The certificates are saved as a PKCS \#7.</span></span><br/> | <span data-ttu-id="8594c-115">1</span><span class="sxs-lookup"><span data-stu-id="8594c-115">1</span></span>     |
| <span data-ttu-id="8594c-116">**CAPICOM \_ Certificates \_ Сохранить \_ как \_ PFX**</span><span class="sxs-lookup"><span data-stu-id="8594c-116">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</span></span>        | <span data-ttu-id="8594c-117">Сертификаты сохраняются в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="8594c-117">The certificates are saved as a PFX.</span></span><br/>      | <span data-ttu-id="8594c-118">2</span><span class="sxs-lookup"><span data-stu-id="8594c-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="8594c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8594c-119">Remarks</span></span>

<span data-ttu-id="8594c-120">\_Тип ПЕРЕЧИСЛЕНИЯ CAPICOM Certificates \_ Save \_ As \_ Type используется методом [**Certificates. Save**](certificates-save.md) .</span><span class="sxs-lookup"><span data-stu-id="8594c-120">The CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration type is used by the [**Certificates.Save**](certificates-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8594c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8594c-121">Requirements</span></span>



| <span data-ttu-id="8594c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8594c-122">Requirement</span></span> | <span data-ttu-id="8594c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8594c-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8594c-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8594c-124">Redistributable</span></span><br/> | <span data-ttu-id="8594c-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="8594c-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="8594c-126">Header</span><span class="sxs-lookup"><span data-stu-id="8594c-126">Header</span></span><br/>          | <dl> <span data-ttu-id="8594c-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8594c-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




