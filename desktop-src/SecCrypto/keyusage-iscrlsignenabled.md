---
description: Получает логическое значение, указывающее, задан ли бит Крлсигн.
ms.assetid: 76ca86e3-55f7-4720-9fa5-d465db2a7b5a
title: Кэйусаже. Искрлсигненаблед, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCRLSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39bd8509ebc89719e5d06e5e60a300ec2cd9949a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665036"
---
# <a name="keyusageiscrlsignenabled-property"></a><span data-ttu-id="55a4d-103">Кэйусаже. Искрлсигненаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="55a4d-103">KeyUsage.IsCRLSignEnabled property</span></span>

<span data-ttu-id="55a4d-104">\[Свойство **искрлсигненаблед** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="55a4d-104">\[The **IsCRLSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55a4d-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="55a4d-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="55a4d-106">Свойство **искрлсигненаблед** Извлекает логическое значение, указывающее, задан ли бит крлсигн.</span><span class="sxs-lookup"><span data-stu-id="55a4d-106">The **IsCRLSignEnabled** property retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a4d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55a4d-107">Syntax</span></span>


```VB
KeyUsage.IsCRLSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="55a4d-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="55a4d-108">Property value</span></span>

<span data-ttu-id="55a4d-109">Если **значение равно true**, бит крлсигн установлен.</span><span class="sxs-lookup"><span data-stu-id="55a4d-109">If **true**, the CRLSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a4d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="55a4d-110">Requirements</span></span>



| <span data-ttu-id="55a4d-111">Требование</span><span class="sxs-lookup"><span data-stu-id="55a4d-111">Requirement</span></span> | <span data-ttu-id="55a4d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="55a4d-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55a4d-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="55a4d-113">Redistributable</span></span><br/> | <span data-ttu-id="55a4d-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="55a4d-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="55a4d-115">DLL</span><span class="sxs-lookup"><span data-stu-id="55a4d-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="55a4d-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a4d-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a4d-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55a4d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a4d-118">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="55a4d-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
