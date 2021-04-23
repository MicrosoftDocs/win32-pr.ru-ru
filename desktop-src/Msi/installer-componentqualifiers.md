---
description: Свойство Компоненткуалифиерс является свойством только для чтения, которое возвращает объект Стринглист, перечисляющий набор зарегистрированных квалификаторов для указанного компонента.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Свойство Installer. Компоненткуалифиерс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651964"
---
# <a name="installercomponentqualifiers-property"></a><span data-ttu-id="46764-103">Свойство Installer. Компоненткуалифиерс</span><span class="sxs-lookup"><span data-stu-id="46764-103">Installer.ComponentQualifiers property</span></span>

<span data-ttu-id="46764-104">Свойство **компоненткуалифиерс** является свойством только для чтения, которое возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор зарегистрированных квалификаторов для указанного компонента.</span><span class="sxs-lookup"><span data-stu-id="46764-104">The **ComponentQualifiers** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of registered qualifiers for the specified component.</span></span>

<span data-ttu-id="46764-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="46764-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46764-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46764-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a><span data-ttu-id="46764-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="46764-107">Property value</span></span>

<span data-ttu-id="46764-108">Строковый идентификатор GUID, представляющий категорию [компонента](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="46764-108">A string GUID that represents the category of [component](publishcomponent-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="46764-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46764-109">Remarks</span></span>

<span data-ttu-id="46764-110">Чтобы перечислить квалификаторы, приложение выполняет итерацию объекта [**стринглист**](stringlist-object.md) , используя для каждой конструкции.</span><span class="sxs-lookup"><span data-stu-id="46764-110">To enumerate qualifiers the application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="46764-111">Поскольку квалификаторы не упорядочены, каждый новый квалификатор имеет произвольный индекс, то есть функция может возвращать квалификаторы в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="46764-111">Because qualifiers are not ordered, any new qualifier has an arbitrary index, meaning the function can return qualifiers in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="46764-112">Требования</span><span class="sxs-lookup"><span data-stu-id="46764-112">Requirements</span></span>



| <span data-ttu-id="46764-113">Требование</span><span class="sxs-lookup"><span data-stu-id="46764-113">Requirement</span></span> | <span data-ttu-id="46764-114">Значение</span><span class="sxs-lookup"><span data-stu-id="46764-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46764-115">Версия</span><span class="sxs-lookup"><span data-stu-id="46764-115">Version</span></span><br/> | <span data-ttu-id="46764-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="46764-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="46764-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="46764-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="46764-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="46764-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="46764-119">DLL</span><span class="sxs-lookup"><span data-stu-id="46764-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="46764-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46764-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="46764-121">IID</span><span class="sxs-lookup"><span data-stu-id="46764-121">IID</span></span><br/>     | <span data-ttu-id="46764-122">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="46764-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="46764-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46764-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46764-124">**мсиенумкомпоненткуалифиерс**</span><span class="sxs-lookup"><span data-stu-id="46764-124">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




