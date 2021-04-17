---
description: Портативные устройства Windows поддерживают следующие свойства ассоциации сети.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Свойства ассоциации сети (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704491"
---
# <a name="network-association-properties"></a><span data-ttu-id="e835b-103">Свойства сетевой ассоциации</span><span class="sxs-lookup"><span data-stu-id="e835b-103">Network Association Properties</span></span>

<span data-ttu-id="e835b-104">Портативные устройства Windows поддерживают следующие свойства ассоциации сети.</span><span class="sxs-lookup"><span data-stu-id="e835b-104">Windows Portable Devices supports the following network association properties.</span></span>



| <span data-ttu-id="e835b-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="e835b-105">Property</span></span>                                                  | <span data-ttu-id="e835b-106">VarType</span><span class="sxs-lookup"><span data-stu-id="e835b-106">VarType</span></span>                   | <span data-ttu-id="e835b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e835b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e835b-108">**\_ \_ \_ \_ идентификаторы сети узла сетевых ассоциаций WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e835b-108">**WPD\_NETWORK\_ASSOCIATION\_HOST\_NETWORK\_IDENTIFIERS**</span></span> | <span data-ttu-id="e835b-109">**VT \_ вектор \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="e835b-109">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="e835b-110">Список идентификаторов узлов EUI-64, допустимых для этой ассоциации. Это массив байтов, содержащий целое число физических сетевых адресов EUI-64.</span><span class="sxs-lookup"><span data-stu-id="e835b-110">The list of EUI-64 host identifiers valid for this association.This is an array of bytes that contains an integral number of EUI-64 physical network addresses.</span></span> <span data-ttu-id="e835b-111">Эти значения EUI-64 — это физические сетевые адреса, доступные на узле во время сетевой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="e835b-111">These EUI-64 values are the physical network addresses available on the host at Network Association time.</span></span> <span data-ttu-id="e835b-112">Если узел имеет физические сетевые адреса MAC-48 (типичные сети IPv4), каждый адрес MAC-48 будет кодироваться в адрес EUI-64, как два половины адреса MAC-48, разделенные FF-FF.</span><span class="sxs-lookup"><span data-stu-id="e835b-112">If the host has MAC-48 physical network addresses (typical of IPv4 networks), each MAC-48 address will be encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span><br/> |
| <span data-ttu-id="e835b-113">**\_X509V3SEQUENCE сетевая \_ Ассоциация WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e835b-113">**WPD\_NETWORK\_ASSOCIATION\_X509V3SEQUENCE**</span></span>             | <span data-ttu-id="e835b-114">**VT \_ вектор \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="e835b-114">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="e835b-115">Последовательность сертификатов X. 509 v3, предоставляемых для проверки подлинности сервера TLS.</span><span class="sxs-lookup"><span data-stu-id="e835b-115">The sequence of X.509 v3 certificates to be provided for TLS server authentication.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="e835b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e835b-116">Requirements</span></span>



| <span data-ttu-id="e835b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e835b-117">Requirement</span></span> | <span data-ttu-id="e835b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e835b-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e835b-119">Header</span><span class="sxs-lookup"><span data-stu-id="e835b-119">Header</span></span><br/> | <dl> <span data-ttu-id="e835b-120"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="e835b-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e835b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e835b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e835b-122">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="e835b-122">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




