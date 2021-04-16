---
description: Возвращает объект Рекордлист, в котором перечислены установленные компоненты.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Свойство Installer. Компонентсекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652073"
---
# <a name="installercomponentsex-property"></a><span data-ttu-id="a38e3-103">Свойство Installer. Компонентсекс</span><span class="sxs-lookup"><span data-stu-id="a38e3-103">Installer.ComponentsEx property</span></span>

<span data-ttu-id="a38e3-104">Это свойство возвращает объект [**рекордлист**](recordlist-object.md) , в котором перечислены установленные компоненты.</span><span class="sxs-lookup"><span data-stu-id="a38e3-104">This property returns a [**RecordList**](recordlist-object.md) object that lists installed components.</span></span> <span data-ttu-id="a38e3-105">Это свойство вызывает [**мсиенумкомпонентсекс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span><span class="sxs-lookup"><span data-stu-id="a38e3-105">This property calls [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span></span>

<span data-ttu-id="a38e3-106">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a38e3-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="a38e3-107">Это свойство доступно, начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="a38e3-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="a38e3-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a38e3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38e3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a38e3-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a><span data-ttu-id="a38e3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a38e3-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a38e3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a38e3-111">Requirements</span></span>



| <span data-ttu-id="a38e3-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a38e3-112">Requirement</span></span> | <span data-ttu-id="a38e3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a38e3-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38e3-114">Версия</span><span class="sxs-lookup"><span data-stu-id="a38e3-114">Version</span></span><br/> | <span data-ttu-id="a38e3-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="a38e3-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="a38e3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a38e3-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="a38e3-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a38e3-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="a38e3-118">IID</span><span class="sxs-lookup"><span data-stu-id="a38e3-118">IID</span></span><br/>     | <span data-ttu-id="a38e3-119">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a38e3-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="a38e3-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a38e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38e3-121">**мсиенумкомпонентсекс**</span><span class="sxs-lookup"><span data-stu-id="a38e3-121">**MsiEnumComponentsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




