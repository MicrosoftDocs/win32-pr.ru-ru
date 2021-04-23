---
description: Возвращает логическое значение, указывающее, предназначен ли сертификат для центра сертификации (ЦС).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: Басикконстраинтс. Исцертификатеаусорити, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669083"
---
# <a name="basicconstraintsiscertificateauthority-property"></a><span data-ttu-id="142b1-103">Басикконстраинтс. Исцертификатеаусорити, свойство</span><span class="sxs-lookup"><span data-stu-id="142b1-103">BasicConstraints.IsCertificateAuthority property</span></span>

<span data-ttu-id="142b1-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="142b1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="142b1-105">Вместо этого используйте [**класс X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="142b1-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="142b1-106">Свойство **исцертификатеаусорити** Извлекает логическое значение, указывающее, предназначен ли сертификат для [*центра сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="142b1-106">The **IsCertificateAuthority** property retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="142b1-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="142b1-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="142b1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="142b1-108">Syntax</span></span>


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a><span data-ttu-id="142b1-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="142b1-109">Property value</span></span>

<span data-ttu-id="142b1-110">Если **значение — true**, сертификат должен использоваться только центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="142b1-110">If **True**, the certificate is to be used only by a CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="142b1-111">Требования</span><span class="sxs-lookup"><span data-stu-id="142b1-111">Requirements</span></span>



| <span data-ttu-id="142b1-112">Требование</span><span class="sxs-lookup"><span data-stu-id="142b1-112">Requirement</span></span> | <span data-ttu-id="142b1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="142b1-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="142b1-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="142b1-114">End of client support</span></span><br/> | <span data-ttu-id="142b1-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="142b1-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="142b1-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="142b1-116">End of server support</span></span><br/> | <span data-ttu-id="142b1-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="142b1-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="142b1-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="142b1-118">Redistributable</span></span><br/>       | <span data-ttu-id="142b1-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="142b1-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="142b1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="142b1-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="142b1-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="142b1-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
