---
description: Получает логическое значение, указывающее, имеется ли расширение базовых ограничений. Это свойство по умолчанию.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: Басикконстраинтс. Present, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9632f0d1297f2effd7d1bcc6056b2327d7f38e26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665529"
---
# <a name="basicconstraintsispresent-property"></a><span data-ttu-id="b6a35-104">Басикконстраинтс. Present, свойство</span><span class="sxs-lookup"><span data-stu-id="b6a35-104">BasicConstraints.IsPresent property</span></span>

<span data-ttu-id="b6a35-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b6a35-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="b6a35-106">Вместо этого используйте [**класс X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="b6a35-106">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="b6a35-107">Свойство **Present** получает логическое значение, указывающее, имеется ли расширение базовых ограничений.</span><span class="sxs-lookup"><span data-stu-id="b6a35-107">The **IsPresent** property retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="b6a35-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b6a35-108">This is the default property.</span></span>

<span data-ttu-id="b6a35-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b6a35-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a35-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6a35-110">Syntax</span></span>


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b6a35-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b6a35-111">Property value</span></span>

<span data-ttu-id="b6a35-112">Если **значение — true**, имеется расширение базовых ограничений.</span><span class="sxs-lookup"><span data-stu-id="b6a35-112">If **true**, the basic constraints extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a35-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b6a35-113">Requirements</span></span>



| <span data-ttu-id="b6a35-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b6a35-114">Requirement</span></span> | <span data-ttu-id="b6a35-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b6a35-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a35-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b6a35-116">End of client support</span></span><br/> | <span data-ttu-id="b6a35-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6a35-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b6a35-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b6a35-118">End of server support</span></span><br/> | <span data-ttu-id="b6a35-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6a35-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b6a35-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b6a35-120">Redistributable</span></span><br/>       | <span data-ttu-id="b6a35-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6a35-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b6a35-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b6a35-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b6a35-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6a35-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a35-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6a35-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a35-125">**басикконстраинтс**</span><span class="sxs-lookup"><span data-stu-id="b6a35-125">**BasicConstraints**</span></span>](basicconstraints.md)
</dt> </dl>

 

 
