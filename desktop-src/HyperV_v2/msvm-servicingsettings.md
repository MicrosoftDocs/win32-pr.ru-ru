---
description: Содержит параметры, используемые во время операций обслуживания.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Класс Msvm_ServicingSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497706"
---
# <a name="msvm_servicingsettings-class"></a><span data-ttu-id="c958a-103">\_Класс мсвм сервиЦингсеттингс</span><span class="sxs-lookup"><span data-stu-id="c958a-103">Msvm\_ServicingSettings class</span></span>

<span data-ttu-id="c958a-104">Содержит параметры, используемые во время операций обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c958a-104">Contains settings used during servicing operations.</span></span>

<span data-ttu-id="c958a-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c958a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c958a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c958a-106">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="c958a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c958a-107">Members</span></span>

<span data-ttu-id="c958a-108">Класс **мсвм \_ сервиЦингсеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c958a-108">The **Msvm\_ServicingSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="c958a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c958a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c958a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c958a-110">Properties</span></span>

<span data-ttu-id="c958a-111">Класс **мсвм \_ сервиЦингсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c958a-111">The **Msvm\_ServicingSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c958a-112">**Version**</span><span class="sxs-lookup"><span data-stu-id="c958a-112">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c958a-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c958a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c958a-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c958a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c958a-115">Содержит версию определения класса.</span><span class="sxs-lookup"><span data-stu-id="c958a-115">Contains the class definition's version.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c958a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c958a-116">Requirements</span></span>



| <span data-ttu-id="c958a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c958a-117">Requirement</span></span> | <span data-ttu-id="c958a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c958a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c958a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c958a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c958a-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c958a-120">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c958a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c958a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c958a-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c958a-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c958a-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c958a-123">Namespace</span></span><br/>                | <span data-ttu-id="c958a-124">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c958a-124">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c958a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c958a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c958a-126"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c958a-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c958a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c958a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c958a-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c958a-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




