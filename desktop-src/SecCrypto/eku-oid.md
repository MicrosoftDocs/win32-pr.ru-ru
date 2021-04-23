---
description: Задает или получает строку, содержащую строковое значение EKU OID, определенное в Винкрипт. h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'Свойство ИЕКУ:: OID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668907"
---
# <a name="iekuoid-property"></a><span data-ttu-id="a685d-103">Свойство ИЕКУ:: OID</span><span class="sxs-lookup"><span data-stu-id="a685d-103">IEKU::OID property</span></span>

<span data-ttu-id="a685d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a685d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a685d-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a685d-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a685d-106">Свойство **OID** задает или получает строку, содержащую строковое значение EKU OID, определенное в винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="a685d-106">The **OID** property sets or retrieves a string that contains an EKU OID string value as defined in Wincrypt.h.</span></span>

<span data-ttu-id="a685d-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a685d-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a685d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a685d-108">Syntax</span></span>


```VB
EKU.OID As String
```



## <a name="property-value"></a><span data-ttu-id="a685d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a685d-109">Property value</span></span>

<span data-ttu-id="a685d-110">Строка, содержащая строковое значение EKU OID, определенное в Винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="a685d-110">String that contains the EKU OID string value as defined in Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="a685d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a685d-111">Remarks</span></span>

<span data-ttu-id="a685d-112">Это свойство не использует объект [**OID**](oid.md) , представленный в элементе CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a685d-112">This property does not use the [**OID**](oid.md) object introduced in CAPICOM 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="a685d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a685d-113">Requirements</span></span>



| <span data-ttu-id="a685d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a685d-114">Requirement</span></span> | <span data-ttu-id="a685d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a685d-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a685d-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a685d-116">End of client support</span></span><br/> | <span data-ttu-id="a685d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a685d-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a685d-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a685d-118">End of server support</span></span><br/> | <span data-ttu-id="a685d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a685d-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a685d-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a685d-120">Redistributable</span></span><br/>       | <span data-ttu-id="a685d-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a685d-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a685d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a685d-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a685d-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a685d-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
