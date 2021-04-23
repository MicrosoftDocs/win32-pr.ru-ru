---
title: Встроенные идентификаторы модулей ключей (Фвпму. h)
description: Идентификаторы модулей ключей, встроенных в платформу фильтрации Windows (WFP), представляются с помощью идентификатора GUID.
ms.assetid: ba3aaf0f-5524-4d61-bb74-e4714b11b2a9
topic_type:
- apiref
api_name:
- FWPM_KEYING_MODULE_IKE
- FWPM_KEYING_MODULE_IKEV2
- FWPM_KEYING_MODULE_AUTHIP
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9e6feb726a62de02130d64cef27cd9078395b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989324"
---
# <a name="built-in-keying-module-identifiers"></a><span data-ttu-id="a3cc3-103">Идентификаторы встроенного модуля создания ключей</span><span class="sxs-lookup"><span data-stu-id="a3cc3-103">Built-in Keying Module Identifiers</span></span>

<span data-ttu-id="a3cc3-104">Идентификаторы модулей ключей, встроенных в платформу фильтрации Windows (WFP), представляются с помощью идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-104">The identifiers for the keying modules that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="a3cc3-105">Эти идентификаторы определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="a3cc3-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**\_ \_ IKE модуля ключей \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="a3cc3-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**FWPM\_KEYING\_MODULE\_IKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3cc3-107">Модуль ключа протокол IKE (IKE).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-107">Internet Key Exchange (IKE) keying module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3cc3-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**\_Модуль ключей \_ фвпм \_ IKEV2**</span><span class="sxs-lookup"><span data-stu-id="a3cc3-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**FWPM\_KEYING\_MODULE\_IKEV2**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3cc3-109">Модуль ключа протокол IKE версии 2 (IKEv2).</span><span class="sxs-lookup"><span data-stu-id="a3cc3-109">Internet Key Exchange version 2 (IKEv2) keying module.</span></span>

> [!Note]  
> <span data-ttu-id="a3cc3-110">Доступно только в Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-110">Available only on Windows Server 2008 R2 and Windows 7.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3cc3-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**\_модуль ключей \_ фвпм \_ AUTHIP**</span><span class="sxs-lookup"><span data-stu-id="a3cc3-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**FWPM\_KEYING\_MODULE\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a3cc3-112">Модуль ключа AuthIP.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-112">AuthIP keying module.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3cc3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a3cc3-113">Requirements</span></span>



| <span data-ttu-id="a3cc3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a3cc3-114">Requirement</span></span> | <span data-ttu-id="a3cc3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a3cc3-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3cc3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3cc3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a3cc3-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3cc3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a3cc3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3cc3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a3cc3-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3cc3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a3cc3-120">Header</span><span class="sxs-lookup"><span data-stu-id="a3cc3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3cc3-121"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3cc3-121"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





