---
description: Представляет необработанные данные из расширенной структуры с расширенными отображаемыми идентификационными данными (E-EDID).
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: Класс WmiMonitorRawEEdidV1Block
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712196"
---
# <a name="wmimonitorraweedidv1block-class"></a><span data-ttu-id="32809-103">Класс WmiMonitorRawEEdidV1Block</span><span class="sxs-lookup"><span data-stu-id="32809-103">WmiMonitorRawEEdidV1Block class</span></span>

<span data-ttu-id="32809-104">Класс WMI **WmiMonitorRawEEdidV1Block** представляет необработанные данные из расширенной структуры с расширенными отображаемыми идентификационными данными (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="32809-104">The **WmiMonitorRawEEdidV1Block** WMI class represents the raw data from a Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span> <span data-ttu-id="32809-105">Эта 128-байтовая структура данных содержит сведения, описывающие оптимальную конфигурацию для дисплея.</span><span class="sxs-lookup"><span data-stu-id="32809-105">This 128-byte data structure contains information that describes the optimal configuration for a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="32809-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32809-106">Syntax</span></span>

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a><span data-ttu-id="32809-107">Члены</span><span class="sxs-lookup"><span data-stu-id="32809-107">Members</span></span>

<span data-ttu-id="32809-108">Класс **WmiMonitorRawEEdidV1Block** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="32809-108">The **WmiMonitorRawEEdidV1Block** class has these types of members:</span></span>

-   [<span data-ttu-id="32809-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="32809-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32809-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="32809-110">Properties</span></span>

<span data-ttu-id="32809-111">Класс **WmiMonitorRawEEdidV1Block** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="32809-111">The **WmiMonitorRawEEdidV1Block** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32809-112">**Активен**</span><span class="sxs-lookup"><span data-stu-id="32809-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32809-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="32809-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32809-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32809-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32809-115">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="32809-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="32809-116">**Содержимое**</span><span class="sxs-lookup"><span data-stu-id="32809-116">**Content**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32809-117">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="32809-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="32809-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32809-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32809-119">128 массив байтов, содержащий необработанное содержимое блока.</span><span class="sxs-lookup"><span data-stu-id="32809-119">128 byte array that contains the raw block content.</span></span>

</dd> <dt>

<span data-ttu-id="32809-120">**Id**</span><span class="sxs-lookup"><span data-stu-id="32809-120">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32809-121">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="32809-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="32809-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32809-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32809-123">Идентификатор блока данных.</span><span class="sxs-lookup"><span data-stu-id="32809-123">Identity of the data block.</span></span>

</dd> <dt>

<span data-ttu-id="32809-124">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="32809-124">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32809-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32809-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32809-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32809-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32809-127">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="32809-127">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="32809-128">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="32809-128">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="32809-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="32809-129">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32809-130">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="32809-130">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="32809-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32809-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32809-132">Тип блока данных.</span><span class="sxs-lookup"><span data-stu-id="32809-132">Type of data block.</span></span> <span data-ttu-id="32809-133">В следующей таблице перечислены возможные значения, которые могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="32809-133">The following table lists possible values that can be returned.</span></span>



| <span data-ttu-id="32809-134">Значение</span><span class="sxs-lookup"><span data-stu-id="32809-134">Value</span></span>                                                                                 | <span data-ttu-id="32809-135">Значение</span><span class="sxs-lookup"><span data-stu-id="32809-135">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="32809-136"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="32809-136"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="32809-137">Не инициализировано</span><span class="sxs-lookup"><span data-stu-id="32809-137">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="32809-138"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="32809-138"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="32809-139">Базовый блок EDID</span><span class="sxs-lookup"><span data-stu-id="32809-139">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="32809-140"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="32809-140"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="32809-141">Блочная схема EDID</span><span class="sxs-lookup"><span data-stu-id="32809-141">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="32809-142"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="32809-142"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="32809-143">Другое</span><span class="sxs-lookup"><span data-stu-id="32809-143">Other</span></span><br/>           |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32809-144">Требования</span><span class="sxs-lookup"><span data-stu-id="32809-144">Requirements</span></span>



| <span data-ttu-id="32809-145">Требование</span><span class="sxs-lookup"><span data-stu-id="32809-145">Requirement</span></span> | <span data-ttu-id="32809-146">Значение</span><span class="sxs-lookup"><span data-stu-id="32809-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32809-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32809-147">Minimum supported client</span></span><br/> | <span data-ttu-id="32809-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32809-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="32809-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32809-149">Minimum supported server</span></span><br/> | <span data-ttu-id="32809-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32809-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="32809-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="32809-151">Namespace</span></span><br/>                | <span data-ttu-id="32809-152">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="32809-152">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="32809-153">MOF</span><span class="sxs-lookup"><span data-stu-id="32809-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32809-154"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32809-154"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="32809-155">DLL</span><span class="sxs-lookup"><span data-stu-id="32809-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32809-156"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32809-156"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32809-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32809-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32809-158">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="32809-158">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="32809-159">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="32809-159">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




