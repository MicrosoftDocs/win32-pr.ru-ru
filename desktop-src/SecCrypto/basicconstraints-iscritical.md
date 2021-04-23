---
description: Получает логическое значение, указывающее, помечено ли расширение базового ограничения как критическое.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: Свойство Басикконстраинтс. Critical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8f3f61a0c458229977abae60258ba4cb71420e72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669082"
---
# <a name="basicconstraintsiscritical-property"></a><span data-ttu-id="03788-103">Свойство Басикконстраинтс. Critical</span><span class="sxs-lookup"><span data-stu-id="03788-103">BasicConstraints.IsCritical property</span></span>

<span data-ttu-id="03788-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="03788-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="03788-105">Вместо этого используйте [**класс X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="03788-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="03788-106">Свойство « **Critical** » получает логическое значение, указывающее, помечено ли расширение базового ограничения как критическое.</span><span class="sxs-lookup"><span data-stu-id="03788-106">The **IsCritical** property retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span>

<span data-ttu-id="03788-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="03788-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03788-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03788-108">Syntax</span></span>


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="03788-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="03788-109">Property value</span></span>

<span data-ttu-id="03788-110">Если **значение — true**, расширение базового ограничения помечается как критическое.</span><span class="sxs-lookup"><span data-stu-id="03788-110">If **true**, the basic constraint extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="03788-111">Требования</span><span class="sxs-lookup"><span data-stu-id="03788-111">Requirements</span></span>



| <span data-ttu-id="03788-112">Требование</span><span class="sxs-lookup"><span data-stu-id="03788-112">Requirement</span></span> | <span data-ttu-id="03788-113">Значение</span><span class="sxs-lookup"><span data-stu-id="03788-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03788-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="03788-114">End of client support</span></span><br/> | <span data-ttu-id="03788-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03788-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="03788-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="03788-116">End of server support</span></span><br/> | <span data-ttu-id="03788-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03788-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="03788-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="03788-118">Redistributable</span></span><br/>       | <span data-ttu-id="03788-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="03788-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="03788-120">DLL</span><span class="sxs-lookup"><span data-stu-id="03788-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="03788-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03788-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
