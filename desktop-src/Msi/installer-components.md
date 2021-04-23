---
description: Свойство "компоненты только для чтения" возвращает объект Стринглист, перечисляющий набор установленных компонентов для всех продуктов.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Свойство Installer. Components
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652074"
---
# <a name="installercomponents-property"></a><span data-ttu-id="11f81-103">Свойство Installer. Components</span><span class="sxs-lookup"><span data-stu-id="11f81-103">Installer.Components property</span></span>

<span data-ttu-id="11f81-104">Свойство " **компоненты** только для чтения" возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор установленных компонентов для всех продуктов.</span><span class="sxs-lookup"><span data-stu-id="11f81-104">The read-only **Components** property returns a [**StringList**](stringlist-object.md) object enumerating the set of installed components for all products.</span></span>

<span data-ttu-id="11f81-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="11f81-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f81-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11f81-106">Syntax</span></span>


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a><span data-ttu-id="11f81-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="11f81-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="11f81-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11f81-108">Remarks</span></span>

<span data-ttu-id="11f81-109">Чтобы перечислить компоненты, приложение может выполнить итерацию по объекту [**стринглист**](stringlist-object.md) , используя для каждой конструкции.</span><span class="sxs-lookup"><span data-stu-id="11f81-109">To enumerate the components, an application can iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="11f81-110">Поскольку компоненты не упорядочены, все новые компоненты имеют произвольный индекс.</span><span class="sxs-lookup"><span data-stu-id="11f81-110">Because components are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="11f81-111">Это означает, что функция может возвращать компоненты в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="11f81-111">This means that the function can return components in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f81-112">Требования</span><span class="sxs-lookup"><span data-stu-id="11f81-112">Requirements</span></span>



| <span data-ttu-id="11f81-113">Требование</span><span class="sxs-lookup"><span data-stu-id="11f81-113">Requirement</span></span> | <span data-ttu-id="11f81-114">Значение</span><span class="sxs-lookup"><span data-stu-id="11f81-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f81-115">Версия</span><span class="sxs-lookup"><span data-stu-id="11f81-115">Version</span></span><br/> | <span data-ttu-id="11f81-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11f81-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="11f81-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11f81-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="11f81-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="11f81-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="11f81-119">DLL</span><span class="sxs-lookup"><span data-stu-id="11f81-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="11f81-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f81-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="11f81-121">IID</span><span class="sxs-lookup"><span data-stu-id="11f81-121">IID</span></span><br/>     | <span data-ttu-id="11f81-122">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="11f81-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="11f81-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11f81-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f81-124">**мсиенумкомпонентс**</span><span class="sxs-lookup"><span data-stu-id="11f81-124">**MsiEnumComponents**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




