---
description: Свойство TargetPath объекта Session — это свойство, доступное для чтения и записи, которое предоставляет полный путь к указанной папке на целевом диске установки.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Свойство Session. TargetPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652243"
---
# <a name="sessiontargetpath-property"></a><span data-ttu-id="80ccb-103">Свойство Session. TargetPath</span><span class="sxs-lookup"><span data-stu-id="80ccb-103">Session.TargetPath property</span></span>

<span data-ttu-id="80ccb-104">Свойство **TargetPath** объекта [**Session**](session-object.md) — это свойство, доступное для чтения и записи, которое предоставляет полный путь к указанной папке на целевом диске установки.</span><span class="sxs-lookup"><span data-stu-id="80ccb-104">The **TargetPath** property of the [**Session**](session-object.md) object is a read-write property that provides the full path to the designated folder on the installation target drive.</span></span>

<span data-ttu-id="80ccb-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="80ccb-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="80ccb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80ccb-106">Syntax</span></span>


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a><span data-ttu-id="80ccb-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="80ccb-107">Property value</span></span>

<span data-ttu-id="80ccb-108">Обязательное с учетом регистра имя свойства папки, заданное первичным ключом [таблицы Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="80ccb-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="80ccb-109">Если папка не существует, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="80ccb-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="80ccb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80ccb-110">Remarks</span></span>

<span data-ttu-id="80ccb-111">Не пытайтесь настроить целевой путь, если компоненты, использующие эти пути, уже установлены для текущего пользователя или для другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="80ccb-111">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="80ccb-112">Проверьте свойство [**продуктстате**](productstate.md) , чтобы определить, установлен ли продукт, содержащий компонент.</span><span class="sxs-lookup"><span data-stu-id="80ccb-112">Check the [**ProductState**](productstate.md) property to determine if the product that contains the component is installed.</span></span>

<span data-ttu-id="80ccb-113">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="80ccb-113">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="80ccb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="80ccb-114">Requirements</span></span>



| <span data-ttu-id="80ccb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="80ccb-115">Requirement</span></span> | <span data-ttu-id="80ccb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="80ccb-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80ccb-117">Версия</span><span class="sxs-lookup"><span data-stu-id="80ccb-117">Version</span></span><br/> | <span data-ttu-id="80ccb-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80ccb-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="80ccb-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="80ccb-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="80ccb-120">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="80ccb-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="80ccb-121">DLL</span><span class="sxs-lookup"><span data-stu-id="80ccb-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="80ccb-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80ccb-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="80ccb-123">IID</span><span class="sxs-lookup"><span data-stu-id="80ccb-123">IID</span></span><br/>     | <span data-ttu-id="80ccb-124">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="80ccb-124">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




