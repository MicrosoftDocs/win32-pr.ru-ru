---
description: Возвращает объект Рекордлист, предоставляющий полный путь к указанному установленному компоненту.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Свойство Installer. Компонентпасекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651965"
---
# <a name="installercomponentpathex-property"></a><span data-ttu-id="c5ad9-103">Свойство Installer. Компонентпасекс</span><span class="sxs-lookup"><span data-stu-id="c5ad9-103">Installer.ComponentPathEx property</span></span>

<span data-ttu-id="c5ad9-104">Это свойство возвращает объект [**рекордлист**](recordlist-object.md) , который предоставляет полный путь к указанному установленному компоненту.</span><span class="sxs-lookup"><span data-stu-id="c5ad9-104">This property returns a [**RecordList**](recordlist-object.md) object that gives the full path of a specified installed component.</span></span> <span data-ttu-id="c5ad9-105">Это свойство вызывает [**мсижеткомпонентпасекс**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span><span class="sxs-lookup"><span data-stu-id="c5ad9-105">This property calls [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span></span>

<span data-ttu-id="c5ad9-106">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5ad9-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="c5ad9-107">Это свойство доступно, начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="c5ad9-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="c5ad9-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c5ad9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ad9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5ad9-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a><span data-ttu-id="c5ad9-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c5ad9-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ad9-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c5ad9-111">Requirements</span></span>



| <span data-ttu-id="c5ad9-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c5ad9-112">Requirement</span></span> | <span data-ttu-id="c5ad9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ad9-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ad9-114">Версия</span><span class="sxs-lookup"><span data-stu-id="c5ad9-114">Version</span></span><br/> | <span data-ttu-id="c5ad9-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5ad9-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="c5ad9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ad9-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5ad9-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5ad9-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="c5ad9-118">IID</span><span class="sxs-lookup"><span data-stu-id="c5ad9-118">IID</span></span><br/>     | <span data-ttu-id="c5ad9-119">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c5ad9-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c5ad9-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5ad9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ad9-121">**мсижеткомпонентпасекс**</span><span class="sxs-lookup"><span data-stu-id="c5ad9-121">**MsiGetComponentPathEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




