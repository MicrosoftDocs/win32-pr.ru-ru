---
description: Свойство "исправления только для чтения" объекта установщика возвращает объект Стринглист, содержащий все исправления, примененные к продукту.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Свойство Installer. Патчs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652169"
---
# <a name="installerpatches-property"></a><span data-ttu-id="7e52a-103">Свойство Installer. Патчs</span><span class="sxs-lookup"><span data-stu-id="7e52a-103">Installer.Patches property</span></span>

<span data-ttu-id="7e52a-104">Свойство " **исправления** только для чтения" объекта [**установщика**](installer-object.md) возвращает объект [**стринглист**](stringlist-object.md) , содержащий все исправления, примененные к продукту.</span><span class="sxs-lookup"><span data-stu-id="7e52a-104">The read-only **Patches** property of the [**Installer**](installer-object.md) object returns a [**StringList**](stringlist-object.md) object that contains all the patches applied to the product.</span></span>

<span data-ttu-id="7e52a-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7e52a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e52a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e52a-106">Syntax</span></span>


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a><span data-ttu-id="7e52a-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7e52a-107">Property value</span></span>

<span data-ttu-id="7e52a-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="7e52a-108">Specifies the product code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e52a-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e52a-109">Remarks</span></span>

<span data-ttu-id="7e52a-110">Чтобы перечислить исправления, приложение выполняет итерацию объекта [**стринглист**](stringlist-object.md) , используя для каждой конструкции.</span><span class="sxs-lookup"><span data-stu-id="7e52a-110">To enumerate the patches, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="7e52a-111">Поскольку исправления не упорядочены, каждое новое исправление имеет произвольный индекс.</span><span class="sxs-lookup"><span data-stu-id="7e52a-111">Because patches are not ordered, any new patch has an arbitrary index.</span></span> <span data-ttu-id="7e52a-112">Это означает, что функция может возвращать исправления в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="7e52a-112">This means that the function can return patches in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e52a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7e52a-113">Requirements</span></span>



| <span data-ttu-id="7e52a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7e52a-114">Requirement</span></span> | <span data-ttu-id="7e52a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7e52a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e52a-116">Версия</span><span class="sxs-lookup"><span data-stu-id="7e52a-116">Version</span></span><br/> | <span data-ttu-id="7e52a-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7e52a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7e52a-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e52a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7e52a-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e52a-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7e52a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7e52a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e52a-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e52a-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7e52a-122">IID</span><span class="sxs-lookup"><span data-stu-id="7e52a-122">IID</span></span><br/>     | <span data-ttu-id="7e52a-123">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7e52a-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="7e52a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e52a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e52a-125">**мсиенумпатчес**</span><span class="sxs-lookup"><span data-stu-id="7e52a-125">**MsiEnumPatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




