---
description: Получает логическое значение, указывающее, задан ли бит Нонрепудиатионенаблед.
ms.assetid: d9bcf0fc-8b2d-408c-b587-71903ef5f5f6
title: Кэйусаже. Иснонрепудиатионенаблед, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsNonRepudiationEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 30e0a532cd39f2150591a3eb74ed9bbba83a7080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665030"
---
# <a name="keyusageisnonrepudiationenabled-property"></a><span data-ttu-id="1614b-103">Кэйусаже. Иснонрепудиатионенаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="1614b-103">KeyUsage.IsNonRepudiationEnabled property</span></span>

<span data-ttu-id="1614b-104">\[Свойство **иснонрепудиатионенаблед** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1614b-104">\[The **IsNonRepudiationEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1614b-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1614b-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1614b-106">Свойство **иснонрепудиатионенаблед** Извлекает логическое значение, указывающее, задан ли бит нонрепудиатионенаблед.</span><span class="sxs-lookup"><span data-stu-id="1614b-106">The **IsNonRepudiationEnabled** property retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="1614b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1614b-107">Syntax</span></span>


```VB
KeyUsage.IsNonRepudiationEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="1614b-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1614b-108">Property value</span></span>

<span data-ttu-id="1614b-109">Если **значение равно true**, бит нонрепудиатионенаблед установлен.</span><span class="sxs-lookup"><span data-stu-id="1614b-109">If **true**, the nonRepudiationEnabled bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1614b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="1614b-110">Requirements</span></span>



| <span data-ttu-id="1614b-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1614b-111">Requirement</span></span> | <span data-ttu-id="1614b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1614b-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1614b-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1614b-113">Redistributable</span></span><br/> | <span data-ttu-id="1614b-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1614b-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1614b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="1614b-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="1614b-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1614b-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1614b-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1614b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1614b-118">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="1614b-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
