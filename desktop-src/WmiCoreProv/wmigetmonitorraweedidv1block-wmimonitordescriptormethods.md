---
description: Получает необработанные данные для указанной расширенной структуры (E-EDID), которая определяет оптимальные параметры для настройки монитора.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Метод WmiGetMonitorRawEEdidV1Block класса Вмимонитордескриптормесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702847"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a><span data-ttu-id="8375d-103">Метод WmiGetMonitorRawEEdidV1Block класса Вмимонитордескриптормесодс</span><span class="sxs-lookup"><span data-stu-id="8375d-103">WmiGetMonitorRawEEdidV1Block method of the WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="8375d-104">Метод **WmiGetMonitorRawEEdidV1Block** получает необработанные данные для указанной расширенной структуры (E-EDID), которая определяет оптимальные параметры для настройки монитора.</span><span class="sxs-lookup"><span data-stu-id="8375d-104">The **WmiGetMonitorRawEEdidV1Block** method gets the raw data for a specified Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure that defines optimal settings for configuring a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="8375d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8375d-105">Syntax</span></span>


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a><span data-ttu-id="8375d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8375d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8375d-107">*ИД блока* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8375d-107">*BlockId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8375d-108">Удостоверение блока данных.</span><span class="sxs-lookup"><span data-stu-id="8375d-108">The data block identity.</span></span>

</dd> <dt>

<span data-ttu-id="8375d-109">*Блокктипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8375d-109">*BlockType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8375d-110">Тип блока данных.</span><span class="sxs-lookup"><span data-stu-id="8375d-110">Type of data block.</span></span> <span data-ttu-id="8375d-111">В следующей таблице перечислены возможные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="8375d-111">The following table lists possible return values.</span></span>



| <span data-ttu-id="8375d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8375d-112">Value</span></span>                                                                                 | <span data-ttu-id="8375d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8375d-113">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="8375d-114"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8375d-114"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="8375d-115">Не инициализировано</span><span class="sxs-lookup"><span data-stu-id="8375d-115">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="8375d-116"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8375d-116"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="8375d-117">Базовый блок EDID</span><span class="sxs-lookup"><span data-stu-id="8375d-117">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="8375d-118"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8375d-118"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="8375d-119">Блочная схема EDID</span><span class="sxs-lookup"><span data-stu-id="8375d-119">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="8375d-120"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="8375d-120"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="8375d-121">Другое</span><span class="sxs-lookup"><span data-stu-id="8375d-121">Other</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="8375d-122">*Блоккконтент* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8375d-122">*BlockContent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8375d-123">128-байтовый массив, содержащий необработанное содержимое блока.</span><span class="sxs-lookup"><span data-stu-id="8375d-123">A 128-byte array that contains the raw block content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8375d-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8375d-124">Return value</span></span>

<span data-ttu-id="8375d-125">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="8375d-125">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="8375d-126">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="8375d-126">Any other number indicates an error.</span></span> <span data-ttu-id="8375d-127">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8375d-127">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="8375d-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="8375d-128">Examples</span></span>

<span data-ttu-id="8375d-129">Следующий пример кода извлекает блоки EDID любого дисплея как необработанные 128 битовых массивов.</span><span class="sxs-lookup"><span data-stu-id="8375d-129">The following code example retrieves the EDID blocks of any display as raw 128 bit arrays.</span></span>


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="8375d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8375d-130">Requirements</span></span>



| <span data-ttu-id="8375d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8375d-131">Requirement</span></span> | <span data-ttu-id="8375d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8375d-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8375d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8375d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8375d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8375d-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8375d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8375d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8375d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8375d-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8375d-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8375d-137">Namespace</span></span><br/>                | <span data-ttu-id="8375d-138">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="8375d-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="8375d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8375d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8375d-140"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8375d-140"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="8375d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8375d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8375d-142"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8375d-142"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8375d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8375d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8375d-144">**вмимонитордескриптормесодс**</span><span class="sxs-lookup"><span data-stu-id="8375d-144">**WmiMonitorDescriptorMethods**</span></span>](wmimonitordescriptormethods.md)
</dt> <dt>

[<span data-ttu-id="8375d-145">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="8375d-145">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

