---
description: Содержит сведения, идентифицирующие адаптер.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: Структура D3DADAPTER_IDENTIFIER9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129973"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="53728-103">\_Структура IDENTIFIER9 D3DADAPTER</span><span class="sxs-lookup"><span data-stu-id="53728-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="53728-104">Содержит сведения, идентифицирующие адаптер.</span><span class="sxs-lookup"><span data-stu-id="53728-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="53728-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53728-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="53728-106">Участники</span><span class="sxs-lookup"><span data-stu-id="53728-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53728-107">**Драйвер**</span><span class="sxs-lookup"><span data-stu-id="53728-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="53728-108">Тип: **char**</span><span class="sxs-lookup"><span data-stu-id="53728-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="53728-109">Используется для представления пользователю.</span><span class="sxs-lookup"><span data-stu-id="53728-109">Used for presentation to the user.</span></span> <span data-ttu-id="53728-110">Это не следует использовать для обнаружения конкретных драйверов, поскольку многие различные строки могут быть связаны с одним и тем же устройством и драйвером от разных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="53728-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="53728-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="53728-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="53728-112">Тип: **char**</span><span class="sxs-lookup"><span data-stu-id="53728-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="53728-113">Используется для представления пользователю.</span><span class="sxs-lookup"><span data-stu-id="53728-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="53728-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="53728-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="53728-115">Тип: **char**</span><span class="sxs-lookup"><span data-stu-id="53728-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="53728-116">Имя устройства для GDI.</span><span class="sxs-lookup"><span data-stu-id="53728-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="53728-117">**дриверверсион**</span><span class="sxs-lookup"><span data-stu-id="53728-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="53728-118">Тип: **[ **большое \_ целое число**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="53728-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-119">Определяет версию драйвера Direct3D.</span><span class="sxs-lookup"><span data-stu-id="53728-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="53728-120">Для 64-разрядного целого числа со знаком допускается меньше и больше сравнений.</span><span class="sxs-lookup"><span data-stu-id="53728-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="53728-121">Однако следует соблюдать осторожность при использовании этого элемента для обнаружения проблемных драйверов.</span><span class="sxs-lookup"><span data-stu-id="53728-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="53728-122">Вместо этого следует использовать Девицеидентифиер.</span><span class="sxs-lookup"><span data-stu-id="53728-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="53728-123">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="53728-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53728-124">**дриверверсионловпарт**</span><span class="sxs-lookup"><span data-stu-id="53728-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="53728-125">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53728-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-126">Определяет версию драйвера Direct3D.</span><span class="sxs-lookup"><span data-stu-id="53728-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="53728-127">Допускается < и > сравнений со значением 64-разрядного целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="53728-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="53728-128">Однако следует соблюдать осторожность при использовании этого элемента для обнаружения проблемных драйверов.</span><span class="sxs-lookup"><span data-stu-id="53728-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="53728-129">Вместо этого следует использовать Девицеидентифиер.</span><span class="sxs-lookup"><span data-stu-id="53728-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="53728-130">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="53728-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53728-131">**дриверверсионхигхпарт**</span><span class="sxs-lookup"><span data-stu-id="53728-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="53728-132">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53728-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-133">Определяет версию драйвера Direct3D.</span><span class="sxs-lookup"><span data-stu-id="53728-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="53728-134">Допускается < и > сравнений со значением 64-разрядного целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="53728-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="53728-135">Однако следует соблюдать осторожность при использовании этого элемента для обнаружения проблемных драйверов.</span><span class="sxs-lookup"><span data-stu-id="53728-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="53728-136">Вместо этого следует использовать Девицеидентифиер.</span><span class="sxs-lookup"><span data-stu-id="53728-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="53728-137">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="53728-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53728-138">**Поставщика**</span><span class="sxs-lookup"><span data-stu-id="53728-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="53728-139">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53728-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-140">Может использоваться для поиска определенного набора микросхем.</span><span class="sxs-lookup"><span data-stu-id="53728-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="53728-141">Запрос этого члена для распознавания изготовителя.</span><span class="sxs-lookup"><span data-stu-id="53728-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="53728-142">Значение может быть равно нулю, если неизвестно.</span><span class="sxs-lookup"><span data-stu-id="53728-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="53728-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="53728-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="53728-144">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53728-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-145">Может использоваться для поиска определенного набора микросхем.</span><span class="sxs-lookup"><span data-stu-id="53728-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="53728-146">Запросите этот элемент, чтобы определить тип набора микросхем.</span><span class="sxs-lookup"><span data-stu-id="53728-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="53728-147">Значение может быть равно нулю, если неизвестно.</span><span class="sxs-lookup"><span data-stu-id="53728-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="53728-148">**субсисид**</span><span class="sxs-lookup"><span data-stu-id="53728-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="53728-149">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53728-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-150">Может использоваться для поиска определенного набора микросхем.</span><span class="sxs-lookup"><span data-stu-id="53728-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="53728-151">Запросите этот элемент, чтобы найти подсистему, как правило, на конкретной доске.</span><span class="sxs-lookup"><span data-stu-id="53728-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="53728-152">Значение может быть равно нулю, если неизвестно.</span><span class="sxs-lookup"><span data-stu-id="53728-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="53728-153">**Редакции**</span><span class="sxs-lookup"><span data-stu-id="53728-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="53728-154">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53728-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-155">Может использоваться для поиска определенного набора микросхем.</span><span class="sxs-lookup"><span data-stu-id="53728-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="53728-156">Запросите этот элемент, чтобы определить уровень редакции набора микросхем.</span><span class="sxs-lookup"><span data-stu-id="53728-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="53728-157">Значение может быть равно нулю, если неизвестно.</span><span class="sxs-lookup"><span data-stu-id="53728-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="53728-158">**девицеидентифиер**</span><span class="sxs-lookup"><span data-stu-id="53728-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="53728-159">Тип: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="53728-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-160">Можно запрашивать для проверки изменений в драйвере и наборе микросхем.</span><span class="sxs-lookup"><span data-stu-id="53728-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="53728-161">Этот идентификатор GUID является уникальным идентификатором для пары "драйвер — набор микросхем".</span><span class="sxs-lookup"><span data-stu-id="53728-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="53728-162">Запросите этот элемент, чтобы отслеживание изменений в драйвере и наборе микросхем, чтобы создать новый профиль для графической подсистемы.</span><span class="sxs-lookup"><span data-stu-id="53728-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="53728-163">Девицеидентифиер также можно использовать для обнаружения определенных проблемных драйверов.</span><span class="sxs-lookup"><span data-stu-id="53728-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="53728-164">**вхкллевел**</span><span class="sxs-lookup"><span data-stu-id="53728-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="53728-165">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53728-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53728-166">Используется для определения уровня проверки лаборатории WHQL для этой пары драйверов и устройств.</span><span class="sxs-lookup"><span data-stu-id="53728-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="53728-167">DWORD — это упакованная структура даты, определяющая дату выпуска последнего теста WHQL, переданного драйвером.</span><span class="sxs-lookup"><span data-stu-id="53728-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="53728-168">В этом значении допускается выполнение < и > операций.</span><span class="sxs-lookup"><span data-stu-id="53728-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="53728-169">Ниже показан формат даты.</span><span class="sxs-lookup"><span data-stu-id="53728-169">The following illustrates the date format.</span></span>



| <span data-ttu-id="53728-170">Bits</span><span class="sxs-lookup"><span data-stu-id="53728-170">Bits</span></span>  |  <span data-ttu-id="53728-171">Описание</span><span class="sxs-lookup"><span data-stu-id="53728-171">Description</span></span>                                             |
|-------|-----------------------------------------------|
| <span data-ttu-id="53728-172">31-16</span><span class="sxs-lookup"><span data-stu-id="53728-172">31-16</span></span> | <span data-ttu-id="53728-173">Год — десятичное число от 1999 до более поздних.</span><span class="sxs-lookup"><span data-stu-id="53728-173">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="53728-174">15-8</span><span class="sxs-lookup"><span data-stu-id="53728-174">15-8</span></span>  | <span data-ttu-id="53728-175">Месяц — десятичное число от 1 до 12.</span><span class="sxs-lookup"><span data-stu-id="53728-175">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="53728-176">7-0</span><span class="sxs-lookup"><span data-stu-id="53728-176">7-0</span></span>   | <span data-ttu-id="53728-177">День — десятичное число от 1 до 31.</span><span class="sxs-lookup"><span data-stu-id="53728-177">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="53728-178">Также используются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="53728-178">The following values are also used.</span></span>



| <span data-ttu-id="53728-179">Значение</span><span class="sxs-lookup"><span data-stu-id="53728-179">Value</span></span>    |  <span data-ttu-id="53728-180">Описание</span><span class="sxs-lookup"><span data-stu-id="53728-180">Description</span></span>                                                     |
|-----|-------------------------------------------------------|
| <span data-ttu-id="53728-181">0</span><span class="sxs-lookup"><span data-stu-id="53728-181">0</span></span>   | <span data-ttu-id="53728-182">Не сертифицировано.</span><span class="sxs-lookup"><span data-stu-id="53728-182">Not certified.</span></span>                                        |
| <span data-ttu-id="53728-183">1</span><span class="sxs-lookup"><span data-stu-id="53728-183">1</span></span>   | <span data-ttu-id="53728-184">Проверка WHQL выполнена, но сведения о датах недоступны.</span><span class="sxs-lookup"><span data-stu-id="53728-184">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="53728-185">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="53728-185">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="53728-186">Для Direct3D9Ex, работающей в Windows Vista, Windows Server 2008, Windows 7 и Windows Server 2008 R2 (или более текущей операционной системы), [**IDirect3D9:: жетадаптеридентифиер**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) возвращает 1 для уровня WHQL без проверки состояния драйвера.</span><span class="sxs-lookup"><span data-stu-id="53728-186">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53728-187">Remarks</span><span class="sxs-lookup"><span data-stu-id="53728-187">Remarks</span></span>

<span data-ttu-id="53728-188">В следующем примере псевдокода показан формат версии, закодированный в элементах Дриверверсион, Дриверверсионловпарт и Дриверверсионхигхпарт.</span><span class="sxs-lookup"><span data-stu-id="53728-188">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="53728-189">Дополнительные сведения о макросе HIWORD, макросе ЛОВОРД и большой целочисленной структуре см. в разделе пакет SDK для платформы \_ .</span><span class="sxs-lookup"><span data-stu-id="53728-189">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="53728-190">Максимальная \_ \_ Строка идентификатора устройства \_ является константой со следующим определением.</span><span class="sxs-lookup"><span data-stu-id="53728-190">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="53728-191">Члены VendorId, DeviceId, Субсисид и Revision можно использовать совместно для обнаружения определенных наборов микросхем.</span><span class="sxs-lookup"><span data-stu-id="53728-191">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="53728-192">Тем не менее, используйте эти члены с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="53728-192">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="53728-193">Требования</span><span class="sxs-lookup"><span data-stu-id="53728-193">Requirements</span></span>



| <span data-ttu-id="53728-194">Требование</span><span class="sxs-lookup"><span data-stu-id="53728-194">Requirement</span></span> | <span data-ttu-id="53728-195">Значение</span><span class="sxs-lookup"><span data-stu-id="53728-195">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53728-196">Заголовок</span><span class="sxs-lookup"><span data-stu-id="53728-196">Header</span></span><br/> | <dl> <span data-ttu-id="53728-197"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="53728-197"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53728-198">См. также</span><span class="sxs-lookup"><span data-stu-id="53728-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53728-199">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="53728-199">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
