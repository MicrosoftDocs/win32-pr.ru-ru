---
description: Свойство Environment объекта Installer — это свойство для чтения и записи, которое является строковым значением для переменной среды текущего процесса.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Свойство установщика. Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651625"
---
# <a name="installerenvironment-property"></a><span data-ttu-id="6d2f1-103">Свойство установщика. Environment</span><span class="sxs-lookup"><span data-stu-id="6d2f1-103">Installer.Environment property</span></span>

<span data-ttu-id="6d2f1-104">Свойство **Environment** объекта [**Installer**](installer-object.md) — это свойство для чтения и записи, которое является строковым значением для переменной среды текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="6d2f1-104">The **Environment** property of the [**Installer**](installer-object.md) object is a read-write property that is the string value for an environment variable of the current process.</span></span>

<span data-ttu-id="6d2f1-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6d2f1-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2f1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d2f1-106">Syntax</span></span>


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a><span data-ttu-id="6d2f1-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6d2f1-107">Property value</span></span>

<span data-ttu-id="6d2f1-108">Имя переменной среды, которая должна быть прочитана или записана.</span><span class="sxs-lookup"><span data-stu-id="6d2f1-108">The name of the environment variable to be read or written.</span></span> <span data-ttu-id="6d2f1-109">Это не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6d2f1-109">This is case-insensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d2f1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d2f1-110">Remarks</span></span>

<span data-ttu-id="6d2f1-111">Установка переменной среды со свойством **Environment** влияет только на активный сеанс.</span><span class="sxs-lookup"><span data-stu-id="6d2f1-111">Setting an environment variable with the **Environment** property only affects the active session.</span></span> <span data-ttu-id="6d2f1-112">Чтобы внести постоянные изменения в переменную среды, используйте [таблицу среда](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="6d2f1-112">To make persistent changes to an environment variable, use the [Environment table](environment-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2f1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6d2f1-113">Requirements</span></span>



| <span data-ttu-id="6d2f1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6d2f1-114">Requirement</span></span> | <span data-ttu-id="6d2f1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2f1-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2f1-116">Версия</span><span class="sxs-lookup"><span data-stu-id="6d2f1-116">Version</span></span><br/> | <span data-ttu-id="6d2f1-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6d2f1-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6d2f1-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6d2f1-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6d2f1-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="6d2f1-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6d2f1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6d2f1-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d2f1-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d2f1-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6d2f1-122">IID</span><span class="sxs-lookup"><span data-stu-id="6d2f1-122">IID</span></span><br/>     | <span data-ttu-id="6d2f1-123">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6d2f1-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




