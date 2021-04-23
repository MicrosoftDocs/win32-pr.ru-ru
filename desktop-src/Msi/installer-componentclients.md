---
description: Свойство Компонентклиентс только для чтения возвращает объект Стринглист, перечисляющий набор клиентов указанного компонента.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Свойство Installer. Компонентклиентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651967"
---
# <a name="installercomponentclients-property"></a><span data-ttu-id="843fa-103">Свойство Installer. Компонентклиентс</span><span class="sxs-lookup"><span data-stu-id="843fa-103">Installer.ComponentClients property</span></span>

<span data-ttu-id="843fa-104">Свойство **компонентклиентс** только для чтения возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор клиентов указанного компонента.</span><span class="sxs-lookup"><span data-stu-id="843fa-104">The read-only **ComponentClients** property returns a [**StringList**](stringlist-object.md) object enumerating the set of clients of a specified component.</span></span>

<span data-ttu-id="843fa-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="843fa-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="843fa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="843fa-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a><span data-ttu-id="843fa-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="843fa-107">Property value</span></span>

<span data-ttu-id="843fa-108">Строковый идентификатор GUID, представляющий код компонента компонента.</span><span class="sxs-lookup"><span data-stu-id="843fa-108">A string GUID that represents the component code of the component.</span></span> <span data-ttu-id="843fa-109">Коды компонентов указываются в столбце ComponentId [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="843fa-109">The component codes are specified in the ComponentId column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="843fa-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="843fa-110">Remarks</span></span>

<span data-ttu-id="843fa-111">Для перечисления клиентов компонентов приложение может выполнить итерацию по объекту [**стринглист**](stringlist-object.md) , используя для каждой конструкции.</span><span class="sxs-lookup"><span data-stu-id="843fa-111">To enumerate the component clients, an application may iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="843fa-112">Так как клиенты не упорядочиваются, все новые компоненты имеют произвольный индекс.</span><span class="sxs-lookup"><span data-stu-id="843fa-112">Because clients are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="843fa-113">Это означает, что функция может возвращать клиентов в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="843fa-113">This means that the function may return clients in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="843fa-114">Требования</span><span class="sxs-lookup"><span data-stu-id="843fa-114">Requirements</span></span>



| <span data-ttu-id="843fa-115">Требование</span><span class="sxs-lookup"><span data-stu-id="843fa-115">Requirement</span></span> | <span data-ttu-id="843fa-116">Значение</span><span class="sxs-lookup"><span data-stu-id="843fa-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="843fa-117">Версия</span><span class="sxs-lookup"><span data-stu-id="843fa-117">Version</span></span><br/> | <span data-ttu-id="843fa-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="843fa-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="843fa-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="843fa-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="843fa-120">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="843fa-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="843fa-121">DLL</span><span class="sxs-lookup"><span data-stu-id="843fa-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="843fa-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="843fa-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="843fa-123">IID</span><span class="sxs-lookup"><span data-stu-id="843fa-123">IID</span></span><br/>     | <span data-ttu-id="843fa-124">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="843fa-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="843fa-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="843fa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843fa-126">**мсиенумклиентс**</span><span class="sxs-lookup"><span data-stu-id="843fa-126">**MsiEnumClients**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




