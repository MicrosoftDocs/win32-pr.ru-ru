---
description: Свойство Продуктинфофромскрипт объекта Installer возвращает значение указанного атрибута, хранящегося в скрипте объявления.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Установщик::P свойство Родуктинфофромскрипт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652224"
---
# <a name="installerproductinfofromscript-property"></a><span data-ttu-id="8ef56-103">Установщик::P свойство Родуктинфофромскрипт</span><span class="sxs-lookup"><span data-stu-id="8ef56-103">Installer::ProductInfoFromScript property</span></span>

<span data-ttu-id="8ef56-104">Свойство **продуктинфофромскрипт** объекта [**Installer**](installer-object.md) возвращает значение указанного атрибута, хранящегося в скрипте объявления.</span><span class="sxs-lookup"><span data-stu-id="8ef56-104">The **ProductInfoFromScript** property of the [**Installer**](installer-object.md) object returns the value of the specified attribute that is stored in an advertise script.</span></span>

<span data-ttu-id="8ef56-105">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="8ef56-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef56-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ef56-106">Syntax</span></span>


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a><span data-ttu-id="8ef56-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8ef56-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ef56-108">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8ef56-108">Error codes</span></span>

<span data-ttu-id="8ef56-109">Строковое или целочисленное значение, зависящее от запрошенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="8ef56-109">A string or integer value depending upon requested attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ef56-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ef56-110">Remarks</span></span>

<span data-ttu-id="8ef56-111">Свойство **продуктинфофромскрипт** использует функцию [**мсижетпродуктинфофромскрипт**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) .</span><span class="sxs-lookup"><span data-stu-id="8ef56-111">The **ProductInfoFromScript** property uses the [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) function.</span></span>

## <a name="examples"></a><span data-ttu-id="8ef56-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="8ef56-112">Examples</span></span>

<span data-ttu-id="8ef56-113">В следующем примере скрипта демонстрируется использование свойства **продуктинфофромскрипт** .</span><span class="sxs-lookup"><span data-stu-id="8ef56-113">The following sample script demonstrates the use of the **ProductInfoFromScript** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a><span data-ttu-id="8ef56-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8ef56-114">Requirements</span></span>



| <span data-ttu-id="8ef56-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8ef56-115">Requirement</span></span> | <span data-ttu-id="8ef56-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef56-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef56-117">Версия</span><span class="sxs-lookup"><span data-stu-id="8ef56-117">Version</span></span><br/> | <span data-ttu-id="8ef56-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8ef56-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8ef56-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8ef56-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8ef56-120">Установщик Windows 4,5 в Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="8ef56-120">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="8ef56-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8ef56-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="8ef56-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ef56-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="8ef56-123">IID</span><span class="sxs-lookup"><span data-stu-id="8ef56-123">IID</span></span><br/>     | <span data-ttu-id="8ef56-124">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8ef56-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="8ef56-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ef56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef56-126">**Установщик**</span><span class="sxs-lookup"><span data-stu-id="8ef56-126">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="8ef56-127">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="8ef56-127">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




