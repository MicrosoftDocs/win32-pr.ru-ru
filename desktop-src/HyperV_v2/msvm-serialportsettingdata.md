---
description: Описание параметров для виртуального последовательного порта.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Класс Msvm_SerialPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910131"
---
# <a name="msvm_serialportsettingdata-class"></a><span data-ttu-id="ba980-103">\_Класс мсвм сериалпортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="ba980-103">Msvm\_SerialPortSettingData class</span></span>

<span data-ttu-id="ba980-104">Описание параметров для виртуального последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="ba980-104">Describes the setting data for a virtual serial port.</span></span>

<span data-ttu-id="ba980-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ba980-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba980-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba980-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a><span data-ttu-id="ba980-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ba980-107">Members</span></span>

<span data-ttu-id="ba980-108">Класс **мсвм \_ сериалпортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ba980-108">The **Msvm\_SerialPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ba980-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba980-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba980-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba980-110">Properties</span></span>

<span data-ttu-id="ba980-111">Класс **мсвм \_ сериалпортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ba980-111">The **Msvm\_SerialPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba980-112">**дебугжермоде**</span><span class="sxs-lookup"><span data-stu-id="ba980-112">**DebuggerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba980-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ba980-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba980-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ba980-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ba980-115">**значение true** , если режим отладчика включен для виртуального последовательного порта; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ba980-115">**true** if the debugger mode is enabled on a virtual serial port; otherwise, **false**.</span></span> <span data-ttu-id="ba980-116">Режим отладчика улучшает использование отладчика ядра Microsoft Windows для виртуального последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="ba980-116">The debugger mode enhances the use of a Microsoft Windows kernel debugger over a virtual serial port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba980-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ba980-117">Requirements</span></span>



| <span data-ttu-id="ba980-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ba980-118">Requirement</span></span> | <span data-ttu-id="ba980-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ba980-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba980-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba980-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ba980-121">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ba980-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ba980-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba980-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ba980-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ba980-123">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ba980-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ba980-124">Namespace</span></span><br/>                | <span data-ttu-id="ba980-125">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ba980-125">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ba980-126">MOF</span><span class="sxs-lookup"><span data-stu-id="ba980-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba980-127"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba980-127"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba980-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ba980-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba980-129"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba980-129"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ba980-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba980-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba980-131">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="ba980-131">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




