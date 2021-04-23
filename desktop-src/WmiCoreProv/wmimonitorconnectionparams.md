---
description: Содержит тип подключения монитора.
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: Класс Вмимониторконнектионпарамс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorConnectionParams
- WmiMonitorConnectionParams.Active
- WmiMonitorConnectionParams.InstanceName
- WmiMonitorConnectionParams.VideoOutputTechnology
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 64212c523459696ced37e42689f6a4be0edb056b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265384"
---
# <a name="wmimonitorconnectionparams-class"></a><span data-ttu-id="8ca1e-103">Класс Вмимониторконнектионпарамс</span><span class="sxs-lookup"><span data-stu-id="8ca1e-103">WmiMonitorConnectionParams class</span></span>

<span data-ttu-id="8ca1e-104">Класс WMI Вмимониторконнектионпарамс содержит тип подключения монитора.</span><span class="sxs-lookup"><span data-stu-id="8ca1e-104">The WmiMonitorConnectionParams WMI class contains the connection type of the monitor.</span></span>

<span data-ttu-id="8ca1e-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8ca1e-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca1e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ca1e-106">Syntax</span></span>

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a><span data-ttu-id="8ca1e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8ca1e-107">Members</span></span>

<span data-ttu-id="8ca1e-108">Класс **вмимониторконнектионпарамс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8ca1e-108">The **WmiMonitorConnectionParams** class has these types of members:</span></span>

-   [<span data-ttu-id="8ca1e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="8ca1e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ca1e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8ca1e-110">Properties</span></span>

<span data-ttu-id="8ca1e-111">Класс **вмимониторконнектионпарамс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8ca1e-111">The **WmiMonitorConnectionParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ca1e-112">**Активен**</span><span class="sxs-lookup"><span data-stu-id="8ca1e-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca1e-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ca1e-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ca1e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ca1e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ca1e-115">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="8ca1e-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="8ca1e-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="8ca1e-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca1e-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ca1e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca1e-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ca1e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ca1e-119">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="8ca1e-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8ca1e-120">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="8ca1e-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="8ca1e-121">**видеуутпуттечнологи**</span><span class="sxs-lookup"><span data-stu-id="8ca1e-121">**VideoOutputTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca1e-122">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ca1e-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca1e-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ca1e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ca1e-124">Тип подключения технологии вывода видео.</span><span class="sxs-lookup"><span data-stu-id="8ca1e-124">Video output technology connection type.</span></span> <span data-ttu-id="8ca1e-125">Допустимые значения описаны в перечислении [ \_ \_ \_ технологии вывода видео D3DKMDT](https://msdn.microsoft.com/library/ms794498.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8ca1e-125">Valid values are documented in the [D3DKMDT\_VIDEO\_OUTPUT\_TECHNOLOGY](https://msdn.microsoft.com/library/ms794498.aspx) enumeration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ca1e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8ca1e-126">Requirements</span></span>



| <span data-ttu-id="8ca1e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8ca1e-127">Requirement</span></span> | <span data-ttu-id="8ca1e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8ca1e-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca1e-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ca1e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca1e-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ca1e-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8ca1e-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ca1e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca1e-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ca1e-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8ca1e-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8ca1e-133">Namespace</span></span><br/>                | <span data-ttu-id="8ca1e-134">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="8ca1e-134">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="8ca1e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8ca1e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ca1e-136"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ca1e-136"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ca1e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8ca1e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ca1e-138"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ca1e-138"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca1e-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ca1e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca1e-140">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="8ca1e-140">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




