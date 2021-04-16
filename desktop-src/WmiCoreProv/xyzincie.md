---
description: Содержит координаты изображения в цветовом пространстве "Международная комиссия по освещения (ЦИЕ) XYZ".
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Класс КсизинЦие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712676"
---
# <a name="xyzincie-class"></a><span data-ttu-id="11bd9-103">Класс КсизинЦие</span><span class="sxs-lookup"><span data-stu-id="11bd9-103">XYZinCIE class</span></span>

<span data-ttu-id="11bd9-104">Класс WMI **ксизинЦие** содержит координаты дисплея в цветовом пространстве «Международная комиссия по освещения (ЦИЕ) XYZ».</span><span class="sxs-lookup"><span data-stu-id="11bd9-104">The **XYZinCIE** WMI class contains the coordinates of the display in the International Commission on Illumination (CIE) XYZ color space.</span></span>

## <a name="syntax"></a><span data-ttu-id="11bd9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11bd9-105">Syntax</span></span>

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a><span data-ttu-id="11bd9-106">Члены</span><span class="sxs-lookup"><span data-stu-id="11bd9-106">Members</span></span>

<span data-ttu-id="11bd9-107">Класс **ксизинЦие** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11bd9-107">The **XYZinCIE** class has these types of members:</span></span>

-   [<span data-ttu-id="11bd9-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="11bd9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11bd9-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="11bd9-109">Properties</span></span>

<span data-ttu-id="11bd9-110">Класс **ксизинЦие** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="11bd9-110">The **XYZinCIE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11bd9-111">**X**</span><span class="sxs-lookup"><span data-stu-id="11bd9-111">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11bd9-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11bd9-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11bd9-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11bd9-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11bd9-114">Координата по оси X.</span><span class="sxs-lookup"><span data-stu-id="11bd9-114">X-coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="11bd9-115">**да**</span><span class="sxs-lookup"><span data-stu-id="11bd9-115">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11bd9-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11bd9-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11bd9-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11bd9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11bd9-118">Координата по оси Y.</span><span class="sxs-lookup"><span data-stu-id="11bd9-118">Y-coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11bd9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11bd9-119">Remarks</span></span>

<span data-ttu-id="11bd9-120">Класс [**вмимониторколорчарактеристикс**](wmimonitorcolorcharacteristics.md) содержит внедренные экземпляры класса **ксизинЦие** для описания цветовых характеристик монитора.</span><span class="sxs-lookup"><span data-stu-id="11bd9-120">The [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) class contains embedded instances of the **XYZinCIE** class to describe the color characteristics of a monitor.</span></span>

<span data-ttu-id="11bd9-121">Чтобы вычислить координату z на основе значений x и y, используйте отношение \| \| (x, y, z) \| \| = 1.</span><span class="sxs-lookup"><span data-stu-id="11bd9-121">To calculate the z-coordinate, based on the x and y values, use the relation \|\|(x,y,z)\|\| = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="11bd9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="11bd9-122">Requirements</span></span>



| <span data-ttu-id="11bd9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="11bd9-123">Requirement</span></span> | <span data-ttu-id="11bd9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="11bd9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11bd9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11bd9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="11bd9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11bd9-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="11bd9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11bd9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="11bd9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11bd9-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="11bd9-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11bd9-129">Namespace</span></span><br/>                | <span data-ttu-id="11bd9-130">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="11bd9-130">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="11bd9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="11bd9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11bd9-132"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11bd9-132"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="11bd9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="11bd9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11bd9-134"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11bd9-134"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11bd9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11bd9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bd9-136">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="11bd9-136">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




