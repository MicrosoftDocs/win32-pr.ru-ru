---
description: Перемещает виртуальный жесткий диск из источника в конечный путь.
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Класс Msvm_MoveUnmanagedVhd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e98139b747f4b32265e27bc84ca240f496dea715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913116"
---
# <a name="msvm_moveunmanagedvhd-class"></a><span data-ttu-id="b8e55-103">\_Класс мсвм мовеунманажедвхд</span><span class="sxs-lookup"><span data-stu-id="b8e55-103">Msvm\_MoveUnmanagedVhd class</span></span>

<span data-ttu-id="b8e55-104">Перемещает виртуальный жесткий диск из источника в конечный путь.</span><span class="sxs-lookup"><span data-stu-id="b8e55-104">Moves a virtual hard drive from the source to the destination path.</span></span>

<span data-ttu-id="b8e55-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b8e55-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e55-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8e55-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="b8e55-107">Члены</span><span class="sxs-lookup"><span data-stu-id="b8e55-107">Members</span></span>

<span data-ttu-id="b8e55-108">Класс **мсвм \_ мовеунманажедвхд** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b8e55-108">The **Msvm\_MoveUnmanagedVhd** class has these types of members:</span></span>

-   [<span data-ttu-id="b8e55-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8e55-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8e55-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8e55-110">Properties</span></span>

<span data-ttu-id="b8e55-111">Класс **мсвм \_ мовеунманажедвхд** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b8e55-111">The **Msvm\_MoveUnmanagedVhd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8e55-112">**вхддестинатионпас**</span><span class="sxs-lookup"><span data-stu-id="b8e55-112">**VhdDestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8e55-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8e55-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8e55-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8e55-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8e55-115">Целевой путь.</span><span class="sxs-lookup"><span data-stu-id="b8e55-115">The destination path.</span></span>

</dd> <dt>

<span data-ttu-id="b8e55-116">**вхдсаурцепас**</span><span class="sxs-lookup"><span data-stu-id="b8e55-116">**VhdSourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8e55-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8e55-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8e55-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8e55-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8e55-119">Исходный путь к перемещаемому виртуальному жесткому диску.</span><span class="sxs-lookup"><span data-stu-id="b8e55-119">The source path of the virtual hard drive to move.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8e55-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b8e55-120">Requirements</span></span>



| <span data-ttu-id="b8e55-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b8e55-121">Requirement</span></span> | <span data-ttu-id="b8e55-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b8e55-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e55-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8e55-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e55-124">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b8e55-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b8e55-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8e55-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e55-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b8e55-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b8e55-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b8e55-127">Namespace</span></span><br/>                | <span data-ttu-id="b8e55-128">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b8e55-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b8e55-129">MOF</span><span class="sxs-lookup"><span data-stu-id="b8e55-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8e55-130"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8e55-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8e55-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b8e55-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8e55-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8e55-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8e55-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8e55-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e55-134">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="b8e55-134">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

 




