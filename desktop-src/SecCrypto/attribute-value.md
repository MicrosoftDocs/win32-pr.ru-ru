---
description: Задает или получает значение атрибута.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Свойство Attribute. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669003"
---
# <a name="attributevalue-property"></a><span data-ttu-id="0f125-103">Свойство Attribute. Value</span><span class="sxs-lookup"><span data-stu-id="0f125-103">Attribute.Value property</span></span>

<span data-ttu-id="0f125-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0f125-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="0f125-105">Вместо этого используйте [**класс криптографикаттрибутеобжект**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="0f125-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="0f125-106">Свойство **value** задает или получает значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="0f125-106">The **Value** property sets or retrieves the value of the attribute.</span></span>

<span data-ttu-id="0f125-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0f125-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f125-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f125-108">Syntax</span></span>


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="0f125-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0f125-109">Property value</span></span>

<span data-ttu-id="0f125-110">Переменная **типа Variant** , которая содержит значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="0f125-110">A **Variant** variable that contains the value of the attribute.</span></span> <span data-ttu-id="0f125-111">Для **атрибутов \_ \_ \_ \_ времени подписи атрибутов CAPICOM, прошедших проверку** , тип данных — **Date**.</span><span class="sxs-lookup"><span data-stu-id="0f125-111">For **CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME** attributes, the data type is **DATE**.</span></span> <span data-ttu-id="0f125-112">Для всех остальных атрибутов значением свойства является строка.</span><span class="sxs-lookup"><span data-stu-id="0f125-112">For all other attributes, the property value is a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f125-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0f125-113">Requirements</span></span>



| <span data-ttu-id="0f125-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0f125-114">Requirement</span></span> | <span data-ttu-id="0f125-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0f125-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f125-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0f125-116">End of client support</span></span><br/> | <span data-ttu-id="0f125-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f125-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0f125-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0f125-118">End of server support</span></span><br/> | <span data-ttu-id="0f125-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f125-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0f125-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0f125-120">Redistributable</span></span><br/>       | <span data-ttu-id="0f125-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0f125-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0f125-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0f125-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0f125-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f125-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
