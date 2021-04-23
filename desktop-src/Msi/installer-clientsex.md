---
description: Возвращает объект Рекордлист, в котором перечислены продукты, использующие указанный установленный компонент.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Свойство Installer. Клиентсекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652024"
---
# <a name="installerclientsex-property"></a><span data-ttu-id="e31a4-103">Свойство Installer. Клиентсекс</span><span class="sxs-lookup"><span data-stu-id="e31a4-103">Installer.ClientsEx property</span></span>

<span data-ttu-id="e31a4-104">Это свойство возвращает объект [**рекордлист**](recordlist-object.md) , в котором перечислены продукты, использующие указанный установленный компонент.</span><span class="sxs-lookup"><span data-stu-id="e31a4-104">This property returns a [**RecordList**](recordlist-object.md) object that lists products that use a specified installed component.</span></span> <span data-ttu-id="e31a4-105">Это свойство вызывает [**мсиенумклиентсекс**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span><span class="sxs-lookup"><span data-stu-id="e31a4-105">This property calls [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span></span>

<span data-ttu-id="e31a4-106">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e31a4-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="e31a4-107">Это свойство доступно, начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="e31a4-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="e31a4-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e31a4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31a4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e31a4-109">Syntax</span></span>


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a><span data-ttu-id="e31a4-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e31a4-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e31a4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="e31a4-111">Requirements</span></span>



| <span data-ttu-id="e31a4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="e31a4-112">Requirement</span></span> | <span data-ttu-id="e31a4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e31a4-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31a4-114">Версия</span><span class="sxs-lookup"><span data-stu-id="e31a4-114">Version</span></span><br/> | <span data-ttu-id="e31a4-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="e31a4-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="e31a4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e31a4-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="e31a4-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31a4-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="e31a4-118">IID</span><span class="sxs-lookup"><span data-stu-id="e31a4-118">IID</span></span><br/>     | <span data-ttu-id="e31a4-119">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e31a4-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="e31a4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e31a4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31a4-121">**мсиенумклиентсекс**</span><span class="sxs-lookup"><span data-stu-id="e31a4-121">**MsiEnumClientsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




