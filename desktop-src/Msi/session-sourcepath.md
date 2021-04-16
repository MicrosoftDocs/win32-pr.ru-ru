---
description: Свойство SourcePath объекта Session является свойством, предназначенным только для чтения и предоставляющим полный путь к указанной папке на исходном носителе или образе сервера.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Свойство Session. SourcePath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679939"
---
# <a name="sessionsourcepath-property"></a><span data-ttu-id="4a778-103">Свойство Session. SourcePath</span><span class="sxs-lookup"><span data-stu-id="4a778-103">Session.SourcePath property</span></span>

<span data-ttu-id="4a778-104">Свойство **SourcePath** объекта [**Session**](session-object.md) является свойством, предназначенным только для чтения и предоставляющим полный путь к указанной папке на исходном носителе или образе сервера.</span><span class="sxs-lookup"><span data-stu-id="4a778-104">The **SourcePath** property of the [**Session**](session-object.md) object is a read-only property that provides the full path to the designated folder on the source media or server image.</span></span>

<span data-ttu-id="4a778-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4a778-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a778-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a778-106">Syntax</span></span>


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a><span data-ttu-id="4a778-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4a778-107">Property value</span></span>

<span data-ttu-id="4a778-108">Обязательное с учетом регистра имя свойства папки, заданное первичным ключом [таблицы Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="4a778-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="4a778-109">Если папка не существует, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="4a778-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a778-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a778-110">Remarks</span></span>

<span data-ttu-id="4a778-111">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="4a778-111">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a778-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4a778-112">Requirements</span></span>



| <span data-ttu-id="4a778-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4a778-113">Requirement</span></span> | <span data-ttu-id="4a778-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4a778-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a778-115">Версия</span><span class="sxs-lookup"><span data-stu-id="4a778-115">Version</span></span><br/> | <span data-ttu-id="4a778-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4a778-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4a778-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4a778-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4a778-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a778-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4a778-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4a778-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4a778-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a778-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4a778-121">IID</span><span class="sxs-lookup"><span data-stu-id="4a778-121">IID</span></span><br/>     | <span data-ttu-id="4a778-122">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4a778-122">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




