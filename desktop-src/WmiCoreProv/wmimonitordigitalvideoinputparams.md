---
description: Представляет входные параметры для цифрового видео.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Класс Вмимонитордигиталвидеоинпутпарамс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712530"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a><span data-ttu-id="c13ef-103">Класс Вмимонитордигиталвидеоинпутпарамс</span><span class="sxs-lookup"><span data-stu-id="c13ef-103">WmiMonitorDigitalVideoInputParams class</span></span>

<span data-ttu-id="c13ef-104">**Вмимонитордигиталвидеоинпутпарамс** представляет входные параметры для цифрового видео.</span><span class="sxs-lookup"><span data-stu-id="c13ef-104">The **WmiMonitorDigitalVideoInputParams** represents input parameters for digital video.</span></span> <span data-ttu-id="c13ef-105">Данные в этом классе соответствуют данным в определении видеовходного видео по стандарту (E-EDID) расширенному расширенному отображению данных.</span><span class="sxs-lookup"><span data-stu-id="c13ef-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="c13ef-106">Экземпляр этого класса доступен только в том случае, если свойство **видеоинпуттипе** класса [**Вмимониторбасикдисплайпарамс**](wmimonitorbasicdisplayparams.md) имеет значение Digital.</span><span class="sxs-lookup"><span data-stu-id="c13ef-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Digital".</span></span>

## <a name="syntax"></a><span data-ttu-id="c13ef-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c13ef-107">Syntax</span></span>

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a><span data-ttu-id="c13ef-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c13ef-108">Members</span></span>

<span data-ttu-id="c13ef-109">Класс **вмимонитордигиталвидеоинпутпарамс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c13ef-109">The **WmiMonitorDigitalVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="c13ef-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c13ef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c13ef-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c13ef-111">Properties</span></span>

<span data-ttu-id="c13ef-112">Класс **вмимонитордигиталвидеоинпутпарамс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c13ef-112">The **WmiMonitorDigitalVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c13ef-113">**Активен**</span><span class="sxs-lookup"><span data-stu-id="c13ef-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13ef-114">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c13ef-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c13ef-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c13ef-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c13ef-116">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="c13ef-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c13ef-117">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="c13ef-117">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13ef-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c13ef-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c13ef-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c13ef-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c13ef-120">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c13ef-120">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c13ef-121">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="c13ef-121">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="c13ef-122">**IsDFP1xCompatible**</span><span class="sxs-lookup"><span data-stu-id="c13ef-122">**IsDFP1xCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13ef-123">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c13ef-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c13ef-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c13ef-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c13ef-125">VESA ДФП 1. x или совместимая.</span><span class="sxs-lookup"><span data-stu-id="c13ef-125">VESA DFP 1.x or compatible.</span></span> <span data-ttu-id="c13ef-126">Если этот параметр задан, интерфейс имеет сигнал совместимости с цифровой плоской панелью VESA (ДФП) 1. x. Переход на более высокий уровень дифференциальной сигнализации (ТМДС) КРГБ, 1 пиксель/час, до 8 бит/цвет, наиболее значимый бит (сверху), с высоким уровнем серьезности, DE-активный.</span><span class="sxs-lookup"><span data-stu-id="c13ef-126">If set, interface is signal compatible with VESA Digital Flat Panel (DFP) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 pixel/clock, up to 8 bits/color most significant bit (MSB) aligned, DE active high.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c13ef-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c13ef-127">Requirements</span></span>



| <span data-ttu-id="c13ef-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c13ef-128">Requirement</span></span> | <span data-ttu-id="c13ef-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c13ef-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c13ef-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c13ef-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c13ef-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c13ef-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c13ef-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c13ef-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c13ef-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c13ef-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c13ef-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c13ef-134">Namespace</span></span><br/>                | <span data-ttu-id="c13ef-135">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="c13ef-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c13ef-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c13ef-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c13ef-137"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c13ef-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c13ef-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c13ef-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c13ef-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c13ef-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c13ef-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c13ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c13ef-141">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="c13ef-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




