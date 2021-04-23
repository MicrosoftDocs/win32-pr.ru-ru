---
description: Получает логическое значение, указывающее, задан ли бит keyEncipherment.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: Кэйусаже. ИскэйенЦиферментенаблед, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665031"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a><span data-ttu-id="c3b18-103">Кэйусаже. ИскэйенЦиферментенаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="c3b18-103">KeyUsage.IsKeyEnciphermentEnabled property</span></span>

<span data-ttu-id="c3b18-104">\[Свойство **искэйенЦиферментенаблед** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="c3b18-104">\[The **IsKeyEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c3b18-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c3b18-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c3b18-106">Свойство **искэйенЦиферментенаблед** Извлекает логическое значение, указывающее, задан ли бит keyEncipherment.</span><span class="sxs-lookup"><span data-stu-id="c3b18-106">The **IsKeyEnciphermentEnabled** property retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3b18-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3b18-107">Syntax</span></span>


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c3b18-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c3b18-108">Property value</span></span>

<span data-ttu-id="c3b18-109">Если **значение равно true**, бит keyEncipherment установлен.</span><span class="sxs-lookup"><span data-stu-id="c3b18-109">If **true**, the keyEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b18-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c3b18-110">Requirements</span></span>



| <span data-ttu-id="c3b18-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c3b18-111">Requirement</span></span> | <span data-ttu-id="c3b18-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c3b18-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b18-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c3b18-113">Redistributable</span></span><br/> | <span data-ttu-id="c3b18-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3b18-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c3b18-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c3b18-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="c3b18-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3b18-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3b18-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3b18-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b18-118">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="c3b18-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
