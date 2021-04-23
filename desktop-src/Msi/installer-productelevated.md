---
description: Свойство Продуктелеватед объекта Installer возвращает значение true, если продукт является управляемым, или значение false, если продукт не является управляемым.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Установщик::P свойство Родуктелеватед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652229"
---
# <a name="installerproductelevated-property"></a><span data-ttu-id="bc511-103">Установщик::P свойство Родуктелеватед</span><span class="sxs-lookup"><span data-stu-id="bc511-103">Installer::ProductElevated property</span></span>

<span data-ttu-id="bc511-104">Свойство **продуктелеватед** объекта [**Installer**](installer-object.md) возвращает значение true, если продукт является управляемым, или значение false, если продукт не является управляемым.</span><span class="sxs-lookup"><span data-stu-id="bc511-104">The **ProductElevated** property of the [**Installer**](installer-object.md) object returns True if the product is managed or False if the product is not managed.</span></span>

<span data-ttu-id="bc511-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bc511-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc511-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc511-106">Syntax</span></span>


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a><span data-ttu-id="bc511-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bc511-107">Property value</span></span>

<span data-ttu-id="bc511-108">Полный идентификатор GUID кода продукта.</span><span class="sxs-lookup"><span data-stu-id="bc511-108">The full product code GUID of the product.</span></span> <span data-ttu-id="bc511-109">Этот параметр обязателен.</span><span class="sxs-lookup"><span data-stu-id="bc511-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc511-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc511-110">Remarks</span></span>

<span data-ttu-id="bc511-111">Свойство **продуктелеватед** использует функцию [**мсииспродуктелеватед**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) .</span><span class="sxs-lookup"><span data-stu-id="bc511-111">The **ProductElevated** property uses the [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) function.</span></span> <span data-ttu-id="bc511-112">Возврат свойства не учитывает политику [AlwaysInstallElevated](alwaysinstallelevated.md) .</span><span class="sxs-lookup"><span data-stu-id="bc511-112">The return of the property does not take into account the [AlwaysInstallElevated](alwaysinstallelevated.md) policy.</span></span>

## <a name="examples"></a><span data-ttu-id="bc511-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="bc511-113">Examples</span></span>

<span data-ttu-id="bc511-114">В следующем примере скрипта демонстрируется использование свойства **продуктелеватед** .</span><span class="sxs-lookup"><span data-stu-id="bc511-114">The following sample script demonstrates the use of the **ProductElevated** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a><span data-ttu-id="bc511-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bc511-115">Requirements</span></span>



| <span data-ttu-id="bc511-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bc511-116">Requirement</span></span> | <span data-ttu-id="bc511-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bc511-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc511-118">Версия</span><span class="sxs-lookup"><span data-stu-id="bc511-118">Version</span></span><br/> | <span data-ttu-id="bc511-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc511-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc511-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc511-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bc511-121">Установщик Windows 4,5 в Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc511-121">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="bc511-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bc511-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc511-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc511-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="bc511-124">IID</span><span class="sxs-lookup"><span data-stu-id="bc511-124">IID</span></span><br/>     | <span data-ttu-id="bc511-125">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bc511-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="bc511-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc511-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc511-127">**Установщик**</span><span class="sxs-lookup"><span data-stu-id="bc511-127">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="bc511-128">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="bc511-128">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




