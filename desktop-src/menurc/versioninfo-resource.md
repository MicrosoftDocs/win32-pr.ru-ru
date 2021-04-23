---
title: Ресурс VERSIONINFO
description: Определяет ресурс сведений о версии. Ресурс содержит такие сведения о файле, как номер версии, требуемая операционная система и исходное имя файла. Ресурс предназначен для использования с функциями сведений о версии.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Меню ресурсов VERSIONINFO и другие ресурсы
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "104339581"
---
# <a name="versioninfo-resource"></a><span data-ttu-id="5a77a-106">Ресурс VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="5a77a-106">VERSIONINFO resource</span></span>

<span data-ttu-id="5a77a-107">Определяет ресурс сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="5a77a-107">Defines a version-information resource.</span></span> <span data-ttu-id="5a77a-108">Ресурс содержит такие сведения о файле, как номер версии, требуемая операционная система и исходное имя файла.</span><span class="sxs-lookup"><span data-stu-id="5a77a-108">The resource contains such information about the file as its version number, its intended operating system, and its original filename.</span></span> <span data-ttu-id="5a77a-109">Ресурс предназначен для использования с функциями [сведений о версии](./version-information.md) .</span><span class="sxs-lookup"><span data-stu-id="5a77a-109">The resource is intended to be used with the [Version Information](./version-information.md) functions.</span></span>

<span data-ttu-id="5a77a-110">Существует два способа форматирования инструкции **versionInfo** :</span><span class="sxs-lookup"><span data-stu-id="5a77a-110">There are two ways to format a **VERSIONINFO** statement:</span></span>

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

<span data-ttu-id="5a77a-111">\- или -</span><span class="sxs-lookup"><span data-stu-id="5a77a-111">\- or -</span></span>

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="5a77a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a77a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a77a-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span><span class="sxs-lookup"><span data-stu-id="5a77a-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-114">Идентификатор ресурса сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="5a77a-114">Version-information resource identifier.</span></span> <span data-ttu-id="5a77a-115">Это значение должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="5a77a-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="5a77a-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*фиксированные сведения*</span><span class="sxs-lookup"><span data-stu-id="5a77a-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-117">Сведения о версии, такие как версия файла и требуемая операционная система.</span><span class="sxs-lookup"><span data-stu-id="5a77a-117">Version information, such as the file version and the intended operating system.</span></span> <span data-ttu-id="5a77a-118">Этот параметр состоит из следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="5a77a-118">This parameter consists of the following statements.</span></span>



| <span data-ttu-id="5a77a-119">Инструкция</span><span class="sxs-lookup"><span data-stu-id="5a77a-119">Statement</span></span>                         | <span data-ttu-id="5a77a-120">Описание</span><span class="sxs-lookup"><span data-stu-id="5a77a-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a77a-121"> *Версия* fileVersion</span><span class="sxs-lookup"><span data-stu-id="5a77a-121">**FILEVERSION** *version*</span></span>         | <span data-ttu-id="5a77a-122">Двоичный номер версии для файла.</span><span class="sxs-lookup"><span data-stu-id="5a77a-122">Binary version number for the file.</span></span> <span data-ttu-id="5a77a-123">*Версия* состоит из 2 32-разрядных целых чисел, определяемых 4 16-разрядными целыми числами.</span><span class="sxs-lookup"><span data-stu-id="5a77a-123">The *version* consists of two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="5a77a-124">Например, "FILEVERSION 3, 10, 0, 61" преобразуется в два даублевордс: 0x0003000a и 0x0000003d в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="5a77a-124">For example, "FILEVERSION 3,10,0,61" is translated into two doublewords: 0x0003000a and 0x0000003d, in that order.</span></span> <span data-ttu-id="5a77a-125">Таким образом, если *версия* определяется значениями **типа DWORD** *сервере dw1* и *Dw2*, они должны появиться в инструкции **FileVersion** следующим образом: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` .</span><span class="sxs-lookup"><span data-stu-id="5a77a-125">Therefore, if *version* is defined by the **DWORD** values *dw1* and *dw2*, they need to appear in the **FILEVERSION** statement as follows: `HIWORD(dw1)`, `LOWORD(dw1)`, `HIWORD(dw2)`, `LOWORD(dw2)`.</span></span> |
| <span data-ttu-id="5a77a-126"> *Версия* PRODUCTVERSION</span><span class="sxs-lookup"><span data-stu-id="5a77a-126">**PRODUCTVERSION** *version*</span></span>      | <span data-ttu-id="5a77a-127">Двоичный номер версии для продукта, с которым распространяется файл.</span><span class="sxs-lookup"><span data-stu-id="5a77a-127">Binary version number for the product with which the file is distributed.</span></span> <span data-ttu-id="5a77a-128">Параметр *Version* — это 2 32-разрядные целые числа, определяемые 4 16-разрядными целыми числами.</span><span class="sxs-lookup"><span data-stu-id="5a77a-128">The *version* parameter is two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="5a77a-129">Дополнительные сведения о *версии* см. в описании **FileVersion** .</span><span class="sxs-lookup"><span data-stu-id="5a77a-129">For more information about *version*, see the **FILEVERSION** description.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="5a77a-130">**Филефлагсмаск** *филефлагсмаск*</span><span class="sxs-lookup"><span data-stu-id="5a77a-130">**FILEFLAGSMASK** *fileflagsmask*</span></span> | <span data-ttu-id="5a77a-131">Указывает, какие биты в инструкции **раздела FILEFLAGS** являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="5a77a-131">Indicates which bits in the **FILEFLAGS** statement are valid.</span></span> <span data-ttu-id="5a77a-132">Для 16-разрядных Windows это значение равно 0x3F.</span><span class="sxs-lookup"><span data-stu-id="5a77a-132">For 16-bit Windows, this value is 0x3f.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5a77a-133">**Раздела FILEFLAGS** *раздела FILEFLAGS*</span><span class="sxs-lookup"><span data-stu-id="5a77a-133">**FILEFLAGS** *fileflags*</span></span>         | <span data-ttu-id="5a77a-134">Атрибуты файла.</span><span class="sxs-lookup"><span data-stu-id="5a77a-134">Attributes of the file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="5a77a-135">**Филеос** *филеос*</span><span class="sxs-lookup"><span data-stu-id="5a77a-135">**FILEOS** *fileos*</span></span>               | <span data-ttu-id="5a77a-136">Операционная система, для которой предназначен этот файл.</span><span class="sxs-lookup"><span data-stu-id="5a77a-136">Operating system for which this file was designed.</span></span> <span data-ttu-id="5a77a-137">Параметр *филеос* может быть одним из значений операционной системы, указанных в разделе «Примечания».</span><span class="sxs-lookup"><span data-stu-id="5a77a-137">The *fileos* parameter can be one of the operating system values given in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5a77a-138"> *Тип* файла тип_файла</span><span class="sxs-lookup"><span data-stu-id="5a77a-138">**FILETYPE** *filetype*</span></span>           | <span data-ttu-id="5a77a-139">Общий тип файла.</span><span class="sxs-lookup"><span data-stu-id="5a77a-139">General type of file.</span></span> <span data-ttu-id="5a77a-140">Параметр *filetype* может иметь одно из значений типа файла, перечисленных в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="5a77a-140">The *filetype* parameter can be one of the file type values listed in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5a77a-141"> *Подтип* филесубтипе</span><span class="sxs-lookup"><span data-stu-id="5a77a-141">**FILESUBTYPE** *subtype*</span></span>         | <span data-ttu-id="5a77a-142">Функция файла.</span><span class="sxs-lookup"><span data-stu-id="5a77a-142">Function of the file.</span></span> <span data-ttu-id="5a77a-143">Параметр *подтипа* равен нулю, если параметр *filetype* в инструкции **filetype** не имеет значение ВФТ \_ drv, ВФТ \_ Font или ВФТ \_ VxD.</span><span class="sxs-lookup"><span data-stu-id="5a77a-143">The *subtype* parameter is zero unless the *filetype* parameter in the **FILETYPE** statement is VFT\_DRV, VFT\_FONT, or VFT\_VXD.</span></span> <span data-ttu-id="5a77a-144">Список значений подтипов файлов см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="5a77a-144">For a list of file subtype values, see the Remarks section.</span></span>                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="5a77a-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*Block-оператор*</span><span class="sxs-lookup"><span data-stu-id="5a77a-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-146">Указывает один или несколько блоков сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="5a77a-146">Specifies one or more version-information blocks.</span></span> <span data-ttu-id="5a77a-147">Блок может содержать строковые сведения или сведения о переменных.</span><span class="sxs-lookup"><span data-stu-id="5a77a-147">A block can contain string information or variable information.</span></span> <span data-ttu-id="5a77a-148">Дополнительные сведения см. в разделе [**блок стрингфилеинфо**](stringfileinfo-block.md) или блок [**варфилеинфо**](varfileinfo-block.md).</span><span class="sxs-lookup"><span data-stu-id="5a77a-148">For more information, see [**StringFileInfo Block**](stringfileinfo-block.md) or [**VarFileInfo Block**](varfileinfo-block.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a77a-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a77a-149">Remarks</span></span>

<span data-ttu-id="5a77a-150">Чтобы использовать константы, указанные в инструкции **versionInfo** , необходимо включить файл заголовков winver. h или Windows. h в файл определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a77a-150">To use the constants specified with the **VERSIONINFO** statement, you must include the Winver.h or Windows.h header file in the resource-definition file.</span></span>

<span data-ttu-id="5a77a-151">В следующем списке описываются параметры, используемые в инструкции **versionInfo** :</span><span class="sxs-lookup"><span data-stu-id="5a77a-151">The following list describes the parameters used in the **VERSIONINFO** statement:</span></span>

<dl> <dt>

<span data-ttu-id="5a77a-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*раздела FILEFLAGS*</span><span class="sxs-lookup"><span data-stu-id="5a77a-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-153">Сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5a77a-153">A combination of the following values.</span></span>



| <span data-ttu-id="5a77a-154">Значение</span><span class="sxs-lookup"><span data-stu-id="5a77a-154">Value</span></span>                      | <span data-ttu-id="5a77a-155">Описание</span><span class="sxs-lookup"><span data-stu-id="5a77a-155">Description</span></span>                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a77a-156">**\_ \_ Отладка VS FF**</span><span class="sxs-lookup"><span data-stu-id="5a77a-156">**VS\_FF\_DEBUG**</span></span>          | <span data-ttu-id="5a77a-157">Файл содержит отладочную информацию или компилируется с включенными функциями отладки.</span><span class="sxs-lookup"><span data-stu-id="5a77a-157">File contains debugging information or is compiled with debugging features enabled.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="5a77a-158">**VS \_ FF \_ исправлено**</span><span class="sxs-lookup"><span data-stu-id="5a77a-158">**VS\_FF\_PATCHED**</span></span>        | <span data-ttu-id="5a77a-159">Файл был изменен и не идентичен исходному файлу отгрузки с тем же номером версии.</span><span class="sxs-lookup"><span data-stu-id="5a77a-159">File has been modified and is not identical to the original shipping file of the same version number.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="5a77a-160">**\_ \_ Предварительный выпуск VS FF**</span><span class="sxs-lookup"><span data-stu-id="5a77a-160">**VS\_FF\_PRERELEASE**</span></span>     | <span data-ttu-id="5a77a-161">Файл является версией для разработки, а не коммерческой выпускаемой продукцией.</span><span class="sxs-lookup"><span data-stu-id="5a77a-161">File is a development version, not a commercially released product.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="5a77a-162">**VS \_ FF \_ приватебуилд**</span><span class="sxs-lookup"><span data-stu-id="5a77a-162">**VS\_FF\_PRIVATEBUILD**</span></span>   | <span data-ttu-id="5a77a-163">Файл не был построен с использованием стандартных процедур выпуска.</span><span class="sxs-lookup"><span data-stu-id="5a77a-163">File was not built using standard release procedures.</span></span> <span data-ttu-id="5a77a-164">Если это значение задано, [**блок стрингфилеинфо**](stringfileinfo-block.md) должен содержать строку **приватебуилд** .</span><span class="sxs-lookup"><span data-stu-id="5a77a-164">If this value is given, the [**StringFileInfo block**](stringfileinfo-block.md) must contain a **PrivateBuild** string.</span></span>                                                                                              |
| <span data-ttu-id="5a77a-165">**VS \_ FF \_ спеЦиалбуилд**</span><span class="sxs-lookup"><span data-stu-id="5a77a-165">**VS\_FF\_SPECIALBUILD**</span></span>   | <span data-ttu-id="5a77a-166">Файл был создан исходной компанией с использованием стандартных процедур выпуска, но является разновидностью стандартного файла с тем же номером версии.</span><span class="sxs-lookup"><span data-stu-id="5a77a-166">File was built by the original company using standard release procedures but is a variation of the standard file of the same version number.</span></span> <span data-ttu-id="5a77a-167">Если это значение задано, блок [блока **стрингфилеинфо**](stringfileinfo-block.md) должен содержать строку **спеЦиалбуилд** .</span><span class="sxs-lookup"><span data-stu-id="5a77a-167">If this value is given, the [**StringFileInfo** block](stringfileinfo-block.md) block must contain a **SpecialBuild** string.</span></span> |
| <span data-ttu-id="5a77a-168">**VS \_ ФФИ \_ филефлагсмаск**</span><span class="sxs-lookup"><span data-stu-id="5a77a-168">**VS\_FFI\_FILEFLAGSMASK**</span></span> | <span data-ttu-id="5a77a-169">Сочетание всех вышеперечисленных значений.</span><span class="sxs-lookup"><span data-stu-id="5a77a-169">A combination of all the preceding values.</span></span>                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="5a77a-170"><span id="fileos"></span><span id="FILEOS"></span>*филеос*</span><span class="sxs-lookup"><span data-stu-id="5a77a-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-171">Одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5a77a-171">One of the following values.</span></span>



| <span data-ttu-id="5a77a-172">Значение</span><span class="sxs-lookup"><span data-stu-id="5a77a-172">Value</span></span>                   | <span data-ttu-id="5a77a-173">Описание</span><span class="sxs-lookup"><span data-stu-id="5a77a-173">Description</span></span>                                                      |
|-------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5a77a-174">**Вос \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="5a77a-174">**VOS\_UNKNOWN**</span></span>        | <span data-ttu-id="5a77a-175">Операционная система, для которой предназначен файл, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="5a77a-175">The operating system for which the file was designed is unknown.</span></span> |
| <span data-ttu-id="5a77a-176">**Вос \_ DOS**</span><span class="sxs-lookup"><span data-stu-id="5a77a-176">**VOS\_DOS**</span></span>            | <span data-ttu-id="5a77a-177">Файл был разработан для MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="5a77a-177">File was designed for MS-DOS.</span></span>                                    |
| <span data-ttu-id="5a77a-178">**Вос \_ NT**</span><span class="sxs-lookup"><span data-stu-id="5a77a-178">**VOS\_NT**</span></span>             | <span data-ttu-id="5a77a-179">Файл был разработан для 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="5a77a-179">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="5a77a-180">**Вос \_ \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="5a77a-180">**VOS\_\_WINDOWS16**</span></span>    | <span data-ttu-id="5a77a-181">Файл был разработан для 16-разрядных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="5a77a-181">File was designed for 16-bit Windows.</span></span>                            |
| <span data-ttu-id="5a77a-182">**Вос \_ \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="5a77a-182">**VOS\_\_WINDOWS32**</span></span>    | <span data-ttu-id="5a77a-183">Файл был разработан для 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="5a77a-183">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="5a77a-184">**Вос \_ DOS \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="5a77a-184">**VOS\_DOS\_WINDOWS16**</span></span> | <span data-ttu-id="5a77a-185">Файл был разработан для 16-разрядных систем Windows, работающих с MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="5a77a-185">File was designed for 16-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="5a77a-186">**Вос \_ DOS \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="5a77a-186">**VOS\_DOS\_WINDOWS32**</span></span> | <span data-ttu-id="5a77a-187">Файл был разработан для 32-разрядной версии Windows, работающей в MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="5a77a-187">File was designed for 32-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="5a77a-188">**Вос \_ NT \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="5a77a-188">**VOS\_NT\_WINDOWS32**</span></span>  | <span data-ttu-id="5a77a-189">Файл был разработан для 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="5a77a-189">File was designed for 32-bit Windows.</span></span>                            |



 

<span data-ttu-id="5a77a-190">Значения 0x00002L, 0x00003L, 0x20000L и 0x30000L зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="5a77a-190">The values 0x00002L, 0x00003L, 0x20000L and 0x30000L are reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5a77a-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span><span class="sxs-lookup"><span data-stu-id="5a77a-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-192">Одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5a77a-192">One of the following values.</span></span>



| <span data-ttu-id="5a77a-193">Значение</span><span class="sxs-lookup"><span data-stu-id="5a77a-193">Value</span></span>                | <span data-ttu-id="5a77a-194">Описание</span><span class="sxs-lookup"><span data-stu-id="5a77a-194">Description</span></span>                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a77a-195">**ВФТ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="5a77a-195">**VFT\_UNKNOWN**</span></span>     | <span data-ttu-id="5a77a-196">Неизвестный тип файла.</span><span class="sxs-lookup"><span data-stu-id="5a77a-196">File type is unknown.</span></span>                                                                                                       |
| <span data-ttu-id="5a77a-197">**\_приложение ВФТ**</span><span class="sxs-lookup"><span data-stu-id="5a77a-197">**VFT\_APP**</span></span>         | <span data-ttu-id="5a77a-198">Файл содержит приложение.</span><span class="sxs-lookup"><span data-stu-id="5a77a-198">File contains an application.</span></span>                                                                                               |
| <span data-ttu-id="5a77a-199">**\_Библиотека DLL ВФТ**</span><span class="sxs-lookup"><span data-stu-id="5a77a-199">**VFT\_DLL**</span></span>         | <span data-ttu-id="5a77a-200">Файл содержит библиотеку динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="5a77a-200">File contains a dynamic-link library (DLL).</span></span>                                                                                 |
| <span data-ttu-id="5a77a-201">**ВФТ \_ DRV**</span><span class="sxs-lookup"><span data-stu-id="5a77a-201">**VFT\_DRV**</span></span>         | <span data-ttu-id="5a77a-202">Файл содержит драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="5a77a-202">File contains a device driver.</span></span> <span data-ttu-id="5a77a-203">Если параметр *filetype* имеет значение **ВФТ \_ DRV**, *подтип* содержит более конкретное описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="5a77a-203">If *filetype* is **VFT\_DRV**, *subtype* contains a more specific description of the driver.</span></span> |
| <span data-ttu-id="5a77a-204">**\_Шрифт ВФТ**</span><span class="sxs-lookup"><span data-stu-id="5a77a-204">**VFT\_FONT**</span></span>        | <span data-ttu-id="5a77a-205">Файл содержит шрифт.</span><span class="sxs-lookup"><span data-stu-id="5a77a-205">File contains a font.</span></span> <span data-ttu-id="5a77a-206">Если параметр *filetype* имеет значение ВФТ \_ Font, *подтип* содержит более конкретное описание шрифта.</span><span class="sxs-lookup"><span data-stu-id="5a77a-206">If *filetype* is VFT\_FONT, *subtype* contains a more specific description of the font.</span></span>               |
| <span data-ttu-id="5a77a-207">**ВФТ \_ VxD**</span><span class="sxs-lookup"><span data-stu-id="5a77a-207">**VFT\_VXD**</span></span>         | <span data-ttu-id="5a77a-208">Файл содержит виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="5a77a-208">File contains a virtual device.</span></span>                                                                                             |
| <span data-ttu-id="5a77a-209">**\_статическая \_ Библиотека ВФТ**</span><span class="sxs-lookup"><span data-stu-id="5a77a-209">**VFT\_STATIC\_LIB**</span></span> | <span data-ttu-id="5a77a-210">Файл содержит библиотеку статической компоновки.</span><span class="sxs-lookup"><span data-stu-id="5a77a-210">File contains a static-link library.</span></span>                                                                                        |



 

<span data-ttu-id="5a77a-211">Все остальные значения зарезервированы для использования корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5a77a-211">All other values are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="5a77a-212"><span id="subtype"></span><span id="SUBTYPE"></span>*Подтип*</span><span class="sxs-lookup"><span data-stu-id="5a77a-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtype*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-213">Дополнительные сведения о типе файлов.</span><span class="sxs-lookup"><span data-stu-id="5a77a-213">Additional information about the file type.</span></span>

<span data-ttu-id="5a77a-214">Если параметр *filetype* задает **ВФТ \_ DRV**, то это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5a77a-214">If *filetype* specifies **VFT\_DRV**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="5a77a-215">Значение</span><span class="sxs-lookup"><span data-stu-id="5a77a-215">Value</span></span>                             | <span data-ttu-id="5a77a-216">Описание</span><span class="sxs-lookup"><span data-stu-id="5a77a-216">Description</span></span>                               |
|-----------------------------------|-------------------------------------------|
| <span data-ttu-id="5a77a-217">**VFT2 \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="5a77a-217">**VFT2\_UNKNOWN**</span></span>                 | <span data-ttu-id="5a77a-218">Неизвестный тип драйвера.</span><span class="sxs-lookup"><span data-stu-id="5a77a-218">Driver type is unknown.</span></span>                   |
| <span data-ttu-id="5a77a-219">**\_Канал VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="5a77a-219">**VFT2\_DRV\_COMM**</span></span>               | <span data-ttu-id="5a77a-220">Файл содержит драйвер связи.</span><span class="sxs-lookup"><span data-stu-id="5a77a-220">File contains a communications driver.</span></span>    |
| <span data-ttu-id="5a77a-221">**\_Принтер VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="5a77a-221">**VFT2\_DRV\_PRINTER**</span></span>            | <span data-ttu-id="5a77a-222">Файл содержит драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="5a77a-222">File contains a printer driver.</span></span>           |
| <span data-ttu-id="5a77a-223">**\_Клавиатура VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="5a77a-223">**VFT2\_DRV\_KEYBOARD**</span></span>           | <span data-ttu-id="5a77a-224">Файл содержит драйвер клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="5a77a-224">File contains a keyboard driver.</span></span>          |
| <span data-ttu-id="5a77a-225">**\_Язык VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="5a77a-225">**VFT2\_DRV\_LANGUAGE**</span></span>           | <span data-ttu-id="5a77a-226">Файл содержит драйвер языка.</span><span class="sxs-lookup"><span data-stu-id="5a77a-226">File contains a language driver.</span></span>          |
| <span data-ttu-id="5a77a-227">**\_Отображение VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="5a77a-227">**VFT2\_DRV\_DISPLAY**</span></span>            | <span data-ttu-id="5a77a-228">Файл содержит драйвер экрана.</span><span class="sxs-lookup"><span data-stu-id="5a77a-228">File contains a display driver.</span></span>           |
| <span data-ttu-id="5a77a-229">**VFT2ая \_ \_ мышь DRV**</span><span class="sxs-lookup"><span data-stu-id="5a77a-229">**VFT2\_DRV\_MOUSE**</span></span>              | <span data-ttu-id="5a77a-230">Файл содержит драйвер мыши.</span><span class="sxs-lookup"><span data-stu-id="5a77a-230">File contains a mouse driver.</span></span>             |
| <span data-ttu-id="5a77a-231">**\_Сеть VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="5a77a-231">**VFT2\_DRV\_NETWORK**</span></span>            | <span data-ttu-id="5a77a-232">Файл содержит сетевой драйвер.</span><span class="sxs-lookup"><span data-stu-id="5a77a-232">File contains a network driver.</span></span>           |
| <span data-ttu-id="5a77a-233">**\_Система VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="5a77a-233">**VFT2\_DRV\_SYSTEM**</span></span>             | <span data-ttu-id="5a77a-234">Файл содержит системный драйвер.</span><span class="sxs-lookup"><span data-stu-id="5a77a-234">File contains a system driver.</span></span>            |
| <span data-ttu-id="5a77a-235">**\_ \_ Устанавливаемый VFT2 DRV**</span><span class="sxs-lookup"><span data-stu-id="5a77a-235">**VFT2\_DRV\_INSTALLABLE**</span></span>        | <span data-ttu-id="5a77a-236">Файл содержит устанавливаемый драйвер.</span><span class="sxs-lookup"><span data-stu-id="5a77a-236">File contains an installable driver.</span></span>      |
| <span data-ttu-id="5a77a-237">**\_Звук VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="5a77a-237">**VFT2\_DRV\_SOUND**</span></span>              | <span data-ttu-id="5a77a-238">Файл содержит звуковой драйвер.</span><span class="sxs-lookup"><span data-stu-id="5a77a-238">File contains a sound driver.</span></span>             |
| <span data-ttu-id="5a77a-239">**\_Принтер с \_ версией VFT2 \_ DRV**</span><span class="sxs-lookup"><span data-stu-id="5a77a-239">**VFT2\_DRV\_VERSIONED\_PRINTER**</span></span> | <span data-ttu-id="5a77a-240">Файл содержит драйвер принтера с версией.</span><span class="sxs-lookup"><span data-stu-id="5a77a-240">File contains a versioned printer driver.</span></span> |



 

<span data-ttu-id="5a77a-241">Если параметр *filetype* задает **\_ Шрифт ВФТ**, то это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5a77a-241">If *filetype* specifies **VFT\_FONT**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="5a77a-242">Значение</span><span class="sxs-lookup"><span data-stu-id="5a77a-242">Value</span></span>                    | <span data-ttu-id="5a77a-243">Описание</span><span class="sxs-lookup"><span data-stu-id="5a77a-243">Description</span></span>                    |
|--------------------------|--------------------------------|
| <span data-ttu-id="5a77a-244">**VFT2 \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="5a77a-244">**VFT2\_UNKNOWN**</span></span>        | <span data-ttu-id="5a77a-245">Неизвестный тип шрифта.</span><span class="sxs-lookup"><span data-stu-id="5a77a-245">Font type is unknown.</span></span>          |
| <span data-ttu-id="5a77a-246">**\_ \_ Растровый шрифт VFT2**</span><span class="sxs-lookup"><span data-stu-id="5a77a-246">**VFT2\_FONT\_RASTER**</span></span>   | <span data-ttu-id="5a77a-247">Файл содержит растровый шрифт.</span><span class="sxs-lookup"><span data-stu-id="5a77a-247">File contains a raster font.</span></span>   |
| <span data-ttu-id="5a77a-248">**\_Вектор ШРИФТА \_ VFT2**</span><span class="sxs-lookup"><span data-stu-id="5a77a-248">**VFT2\_FONT\_VECTOR**</span></span>   | <span data-ttu-id="5a77a-249">Файл содержит векторный шрифт.</span><span class="sxs-lookup"><span data-stu-id="5a77a-249">File contains a vector font.</span></span>   |
| <span data-ttu-id="5a77a-250">**VFT2 \_ шрифт \_ TRUETYPE**</span><span class="sxs-lookup"><span data-stu-id="5a77a-250">**VFT2\_FONT\_TRUETYPE**</span></span> | <span data-ttu-id="5a77a-251">Файл содержит шрифт TrueType.</span><span class="sxs-lookup"><span data-stu-id="5a77a-251">File contains a TrueType font.</span></span> |



 

<span data-ttu-id="5a77a-252">Если параметр *filetype* указывает ВФТ \_ VxD, то это должен быть идентификатор виртуального устройства, который входит в блок управления виртуальным устройством.</span><span class="sxs-lookup"><span data-stu-id="5a77a-252">If *filetype* specifies VFT\_VXD, this parameter must be the virtual-device identifier included in the virtual-device control block.</span></span>

<span data-ttu-id="5a77a-253">Все значения *подтипа* , не указанные здесь, зарезервированы для использования корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5a77a-253">All *subtype* values not listed here are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="5a77a-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Надежно*</span><span class="sxs-lookup"><span data-stu-id="5a77a-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-255">Один из следующих кодов языка.</span><span class="sxs-lookup"><span data-stu-id="5a77a-255">One of the following language codes.</span></span>



| <span data-ttu-id="5a77a-256">Код</span><span class="sxs-lookup"><span data-stu-id="5a77a-256">Code</span></span>   | <span data-ttu-id="5a77a-257">Язык</span><span class="sxs-lookup"><span data-stu-id="5a77a-257">Language</span></span>            | <span data-ttu-id="5a77a-258">Код</span><span class="sxs-lookup"><span data-stu-id="5a77a-258">Code</span></span>   | <span data-ttu-id="5a77a-259">Язык</span><span class="sxs-lookup"><span data-stu-id="5a77a-259">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="5a77a-260">0x0401</span><span class="sxs-lookup"><span data-stu-id="5a77a-260">0x0401</span></span> | <span data-ttu-id="5a77a-261">Арабский</span><span class="sxs-lookup"><span data-stu-id="5a77a-261">Arabic</span></span>              | <span data-ttu-id="5a77a-262">0x0415</span><span class="sxs-lookup"><span data-stu-id="5a77a-262">0x0415</span></span> | <span data-ttu-id="5a77a-263">Польский</span><span class="sxs-lookup"><span data-stu-id="5a77a-263">Polish</span></span>                    |
| <span data-ttu-id="5a77a-264">0x0402</span><span class="sxs-lookup"><span data-stu-id="5a77a-264">0x0402</span></span> | <span data-ttu-id="5a77a-265">Болгарский</span><span class="sxs-lookup"><span data-stu-id="5a77a-265">Bulgarian</span></span>           | <span data-ttu-id="5a77a-266">0x0416</span><span class="sxs-lookup"><span data-stu-id="5a77a-266">0x0416</span></span> | <span data-ttu-id="5a77a-267">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="5a77a-267">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="5a77a-268">0x0403</span><span class="sxs-lookup"><span data-stu-id="5a77a-268">0x0403</span></span> | <span data-ttu-id="5a77a-269">Каталонский</span><span class="sxs-lookup"><span data-stu-id="5a77a-269">Catalan</span></span>             | <span data-ttu-id="5a77a-270">0x0417</span><span class="sxs-lookup"><span data-stu-id="5a77a-270">0x0417</span></span> | <span data-ttu-id="5a77a-271">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="5a77a-271">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="5a77a-272">0x0404</span><span class="sxs-lookup"><span data-stu-id="5a77a-272">0x0404</span></span> | <span data-ttu-id="5a77a-273">Китайский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="5a77a-273">Traditional Chinese</span></span> | <span data-ttu-id="5a77a-274">0x0418</span><span class="sxs-lookup"><span data-stu-id="5a77a-274">0x0418</span></span> | <span data-ttu-id="5a77a-275">Румынский</span><span class="sxs-lookup"><span data-stu-id="5a77a-275">Romanian</span></span>                  |
| <span data-ttu-id="5a77a-276">0x0405</span><span class="sxs-lookup"><span data-stu-id="5a77a-276">0x0405</span></span> | <span data-ttu-id="5a77a-277">Чешский</span><span class="sxs-lookup"><span data-stu-id="5a77a-277">Czech</span></span>               | <span data-ttu-id="5a77a-278">0x0419</span><span class="sxs-lookup"><span data-stu-id="5a77a-278">0x0419</span></span> | <span data-ttu-id="5a77a-279">русском языке</span><span class="sxs-lookup"><span data-stu-id="5a77a-279">Russian</span></span>                   |
| <span data-ttu-id="5a77a-280">0x0406</span><span class="sxs-lookup"><span data-stu-id="5a77a-280">0x0406</span></span> | <span data-ttu-id="5a77a-281">Датский</span><span class="sxs-lookup"><span data-stu-id="5a77a-281">Danish</span></span>              | <span data-ttu-id="5a77a-282">0x041A</span><span class="sxs-lookup"><span data-stu-id="5a77a-282">0x041A</span></span> | <span data-ttu-id="5a77a-283">Croato-Serbian (латиница)</span><span class="sxs-lookup"><span data-stu-id="5a77a-283">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="5a77a-284">0x0407</span><span class="sxs-lookup"><span data-stu-id="5a77a-284">0x0407</span></span> | <span data-ttu-id="5a77a-285">Немецкий</span><span class="sxs-lookup"><span data-stu-id="5a77a-285">German</span></span>              | <span data-ttu-id="5a77a-286">0x041B</span><span class="sxs-lookup"><span data-stu-id="5a77a-286">0x041B</span></span> | <span data-ttu-id="5a77a-287">Словацкий</span><span class="sxs-lookup"><span data-stu-id="5a77a-287">Slovak</span></span>                    |
| <span data-ttu-id="5a77a-288">0x0408</span><span class="sxs-lookup"><span data-stu-id="5a77a-288">0x0408</span></span> | <span data-ttu-id="5a77a-289">Греческий</span><span class="sxs-lookup"><span data-stu-id="5a77a-289">Greek</span></span>               | <span data-ttu-id="5a77a-290">0x041C</span><span class="sxs-lookup"><span data-stu-id="5a77a-290">0x041C</span></span> | <span data-ttu-id="5a77a-291">Албанский</span><span class="sxs-lookup"><span data-stu-id="5a77a-291">Albanian</span></span>                  |
| <span data-ttu-id="5a77a-292">0x0409</span><span class="sxs-lookup"><span data-stu-id="5a77a-292">0x0409</span></span> | <span data-ttu-id="5a77a-293">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="5a77a-293">U.S. English</span></span>        | <span data-ttu-id="5a77a-294">0x041D</span><span class="sxs-lookup"><span data-stu-id="5a77a-294">0x041D</span></span> | <span data-ttu-id="5a77a-295">Шведский</span><span class="sxs-lookup"><span data-stu-id="5a77a-295">Swedish</span></span>                   |
| <span data-ttu-id="5a77a-296">0x040A</span><span class="sxs-lookup"><span data-stu-id="5a77a-296">0x040A</span></span> | <span data-ttu-id="5a77a-297">Кастильский испанский</span><span class="sxs-lookup"><span data-stu-id="5a77a-297">Castilian Spanish</span></span>   | <span data-ttu-id="5a77a-298">0x041E</span><span class="sxs-lookup"><span data-stu-id="5a77a-298">0x041E</span></span> | <span data-ttu-id="5a77a-299">Тайский</span><span class="sxs-lookup"><span data-stu-id="5a77a-299">Thai</span></span>                      |
| <span data-ttu-id="5a77a-300">0x040B</span><span class="sxs-lookup"><span data-stu-id="5a77a-300">0x040B</span></span> | <span data-ttu-id="5a77a-301">Финский</span><span class="sxs-lookup"><span data-stu-id="5a77a-301">Finnish</span></span>             | <span data-ttu-id="5a77a-302">0x041F</span><span class="sxs-lookup"><span data-stu-id="5a77a-302">0x041F</span></span> | <span data-ttu-id="5a77a-303">Турецкий</span><span class="sxs-lookup"><span data-stu-id="5a77a-303">Turkish</span></span>                   |
| <span data-ttu-id="5a77a-304">0x040C</span><span class="sxs-lookup"><span data-stu-id="5a77a-304">0x040C</span></span> | <span data-ttu-id="5a77a-305">Французский</span><span class="sxs-lookup"><span data-stu-id="5a77a-305">French</span></span>              | <span data-ttu-id="5a77a-306">0x0420</span><span class="sxs-lookup"><span data-stu-id="5a77a-306">0x0420</span></span> | <span data-ttu-id="5a77a-307">Урду</span><span class="sxs-lookup"><span data-stu-id="5a77a-307">Urdu</span></span>                      |
| <span data-ttu-id="5a77a-308">0x040D</span><span class="sxs-lookup"><span data-stu-id="5a77a-308">0x040D</span></span> | <span data-ttu-id="5a77a-309">Иврит</span><span class="sxs-lookup"><span data-stu-id="5a77a-309">Hebrew</span></span>              | <span data-ttu-id="5a77a-310">0x0421</span><span class="sxs-lookup"><span data-stu-id="5a77a-310">0x0421</span></span> | <span data-ttu-id="5a77a-311">Бахаса</span><span class="sxs-lookup"><span data-stu-id="5a77a-311">Bahasa</span></span>                    |
| <span data-ttu-id="5a77a-312">0x040E</span><span class="sxs-lookup"><span data-stu-id="5a77a-312">0x040E</span></span> | <span data-ttu-id="5a77a-313">Венгерский</span><span class="sxs-lookup"><span data-stu-id="5a77a-313">Hungarian</span></span>           | <span data-ttu-id="5a77a-314">0x0804</span><span class="sxs-lookup"><span data-stu-id="5a77a-314">0x0804</span></span> | <span data-ttu-id="5a77a-315">Китайский (упрощенный)</span><span class="sxs-lookup"><span data-stu-id="5a77a-315">Simplified Chinese</span></span>        |
| <span data-ttu-id="5a77a-316">0x040F</span><span class="sxs-lookup"><span data-stu-id="5a77a-316">0x040F</span></span> | <span data-ttu-id="5a77a-317">Исландский</span><span class="sxs-lookup"><span data-stu-id="5a77a-317">Icelandic</span></span>           | <span data-ttu-id="5a77a-318">0x0807</span><span class="sxs-lookup"><span data-stu-id="5a77a-318">0x0807</span></span> | <span data-ttu-id="5a77a-319">Швейцарская немецкая</span><span class="sxs-lookup"><span data-stu-id="5a77a-319">Swiss German</span></span>              |
| <span data-ttu-id="5a77a-320">0x0410</span><span class="sxs-lookup"><span data-stu-id="5a77a-320">0x0410</span></span> | <span data-ttu-id="5a77a-321">Итальянский</span><span class="sxs-lookup"><span data-stu-id="5a77a-321">Italian</span></span>             | <span data-ttu-id="5a77a-322">0x0809</span><span class="sxs-lookup"><span data-stu-id="5a77a-322">0x0809</span></span> | <span data-ttu-id="5a77a-323">Великобритании</span><span class="sxs-lookup"><span data-stu-id="5a77a-323">U.K.</span></span> <span data-ttu-id="5a77a-324">Английский</span><span class="sxs-lookup"><span data-stu-id="5a77a-324">English</span></span>              |
| <span data-ttu-id="5a77a-325">0x0411</span><span class="sxs-lookup"><span data-stu-id="5a77a-325">0x0411</span></span> | <span data-ttu-id="5a77a-326">Японский</span><span class="sxs-lookup"><span data-stu-id="5a77a-326">Japanese</span></span>            | <span data-ttu-id="5a77a-327">0x080A</span><span class="sxs-lookup"><span data-stu-id="5a77a-327">0x080A</span></span> | <span data-ttu-id="5a77a-328">Испанский (Мексика)</span><span class="sxs-lookup"><span data-stu-id="5a77a-328">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="5a77a-329">0x0412</span><span class="sxs-lookup"><span data-stu-id="5a77a-329">0x0412</span></span> | <span data-ttu-id="5a77a-330">Корейский</span><span class="sxs-lookup"><span data-stu-id="5a77a-330">Korean</span></span>              | <span data-ttu-id="5a77a-331">0x080C</span><span class="sxs-lookup"><span data-stu-id="5a77a-331">0x080C</span></span> | <span data-ttu-id="5a77a-332">Бельгия (французский)</span><span class="sxs-lookup"><span data-stu-id="5a77a-332">Belgian French</span></span>            |
| <span data-ttu-id="5a77a-333">0x0413</span><span class="sxs-lookup"><span data-stu-id="5a77a-333">0x0413</span></span> | <span data-ttu-id="5a77a-334">Нидерландский</span><span class="sxs-lookup"><span data-stu-id="5a77a-334">Dutch</span></span>               | <span data-ttu-id="5a77a-335">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="5a77a-335">0x0C0C</span></span> | <span data-ttu-id="5a77a-336">Французский (Канада)</span><span class="sxs-lookup"><span data-stu-id="5a77a-336">Canadian French</span></span>           |
| <span data-ttu-id="5a77a-337">0x0414</span><span class="sxs-lookup"><span data-stu-id="5a77a-337">0x0414</span></span> | <span data-ttu-id="5a77a-338">норвежский?</span><span class="sxs-lookup"><span data-stu-id="5a77a-338">Norwegian ?</span></span> <span data-ttu-id="5a77a-339">Букмол</span><span class="sxs-lookup"><span data-stu-id="5a77a-339">Bokmal</span></span>  | <span data-ttu-id="5a77a-340">0x100C</span><span class="sxs-lookup"><span data-stu-id="5a77a-340">0x100C</span></span> | <span data-ttu-id="5a77a-341">Швейцарский французский</span><span class="sxs-lookup"><span data-stu-id="5a77a-341">Swiss French</span></span>              |
| <span data-ttu-id="5a77a-342">0x0810</span><span class="sxs-lookup"><span data-stu-id="5a77a-342">0x0810</span></span> | <span data-ttu-id="5a77a-343">Швейцарский итальянский</span><span class="sxs-lookup"><span data-stu-id="5a77a-343">Swiss Italian</span></span>       | <span data-ttu-id="5a77a-344">0x0816</span><span class="sxs-lookup"><span data-stu-id="5a77a-344">0x0816</span></span> | <span data-ttu-id="5a77a-345">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="5a77a-345">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="5a77a-346">0x0813</span><span class="sxs-lookup"><span data-stu-id="5a77a-346">0x0813</span></span> | <span data-ttu-id="5a77a-347">Голландский (Бельгия)</span><span class="sxs-lookup"><span data-stu-id="5a77a-347">Belgian Dutch</span></span>       | <span data-ttu-id="5a77a-348">0x081A</span><span class="sxs-lookup"><span data-stu-id="5a77a-348">0x081A</span></span> | <span data-ttu-id="5a77a-349">Serbo-Croatian (кириллица)</span><span class="sxs-lookup"><span data-stu-id="5a77a-349">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="5a77a-350">0x0814</span><span class="sxs-lookup"><span data-stu-id="5a77a-350">0x0814</span></span> | <span data-ttu-id="5a77a-351">норвежский?</span><span class="sxs-lookup"><span data-stu-id="5a77a-351">Norwegian ?</span></span> <span data-ttu-id="5a77a-352">Нюнорск</span><span class="sxs-lookup"><span data-stu-id="5a77a-352">Nynorsk</span></span> |        |                           |



 

</dd> <dt>

<span data-ttu-id="5a77a-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*чарсетид*</span><span class="sxs-lookup"><span data-stu-id="5a77a-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-354">Один из следующих идентификаторов наборов символов.</span><span class="sxs-lookup"><span data-stu-id="5a77a-354">One of the following character-set identifiers.</span></span>



| <span data-ttu-id="5a77a-355">Decimal</span><span class="sxs-lookup"><span data-stu-id="5a77a-355">Decimal</span></span> | <span data-ttu-id="5a77a-356">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="5a77a-356">Hexadecimal</span></span> | <span data-ttu-id="5a77a-357">Кодировка</span><span class="sxs-lookup"><span data-stu-id="5a77a-357">Character Set</span></span>              |
|---------|-------------|----------------------------|
| <span data-ttu-id="5a77a-358">0</span><span class="sxs-lookup"><span data-stu-id="5a77a-358">0</span></span>       | <span data-ttu-id="5a77a-359">0000</span><span class="sxs-lookup"><span data-stu-id="5a77a-359">0000</span></span>        | <span data-ttu-id="5a77a-360">7-разрядный код ASCII</span><span class="sxs-lookup"><span data-stu-id="5a77a-360">7-bit ASCII</span></span>                |
| <span data-ttu-id="5a77a-361">932</span><span class="sxs-lookup"><span data-stu-id="5a77a-361">932</span></span>     | <span data-ttu-id="5a77a-362">03A4</span><span class="sxs-lookup"><span data-stu-id="5a77a-362">03A4</span></span>        | <span data-ttu-id="5a77a-363">Япония (Shift?</span><span class="sxs-lookup"><span data-stu-id="5a77a-363">Japan (Shift ?</span></span> <span data-ttu-id="5a77a-364">JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="5a77a-364">JIS X-0208)</span></span> |
| <span data-ttu-id="5a77a-365">949</span><span class="sxs-lookup"><span data-stu-id="5a77a-365">949</span></span>     | <span data-ttu-id="5a77a-366">03B5</span><span class="sxs-lookup"><span data-stu-id="5a77a-366">03B5</span></span>        | <span data-ttu-id="5a77a-367">Корея (Shift)?</span><span class="sxs-lookup"><span data-stu-id="5a77a-367">Korea (Shift ?</span></span> <span data-ttu-id="5a77a-368">КСК 5601)</span><span class="sxs-lookup"><span data-stu-id="5a77a-368">KSC 5601)</span></span>   |
| <span data-ttu-id="5a77a-369">950</span><span class="sxs-lookup"><span data-stu-id="5a77a-369">950</span></span>     | <span data-ttu-id="5a77a-370">03B6</span><span class="sxs-lookup"><span data-stu-id="5a77a-370">03B6</span></span>        | <span data-ttu-id="5a77a-371">Тайвань (Big5)</span><span class="sxs-lookup"><span data-stu-id="5a77a-371">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="5a77a-372">1200</span><span class="sxs-lookup"><span data-stu-id="5a77a-372">1200</span></span>    | <span data-ttu-id="5a77a-373">04B0</span><span class="sxs-lookup"><span data-stu-id="5a77a-373">04B0</span></span>        | <span data-ttu-id="5a77a-374">Юникод</span><span class="sxs-lookup"><span data-stu-id="5a77a-374">Unicode</span></span>                    |
| <span data-ttu-id="5a77a-375">1250</span><span class="sxs-lookup"><span data-stu-id="5a77a-375">1250</span></span>    | <span data-ttu-id="5a77a-376">04E2</span><span class="sxs-lookup"><span data-stu-id="5a77a-376">04E2</span></span>        | <span data-ttu-id="5a77a-377">Латиница 2 (Восточная Европа)</span><span class="sxs-lookup"><span data-stu-id="5a77a-377">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="5a77a-378">1251</span><span class="sxs-lookup"><span data-stu-id="5a77a-378">1251</span></span>    | <span data-ttu-id="5a77a-379">04E3</span><span class="sxs-lookup"><span data-stu-id="5a77a-379">04E3</span></span>        | <span data-ttu-id="5a77a-380">Кириллица</span><span class="sxs-lookup"><span data-stu-id="5a77a-380">Cyrillic</span></span>                   |
| <span data-ttu-id="5a77a-381">1252</span><span class="sxs-lookup"><span data-stu-id="5a77a-381">1252</span></span>    | <span data-ttu-id="5a77a-382">04E4</span><span class="sxs-lookup"><span data-stu-id="5a77a-382">04E4</span></span>        | <span data-ttu-id="5a77a-383">Многоязычных</span><span class="sxs-lookup"><span data-stu-id="5a77a-383">Multilingual</span></span>               |
| <span data-ttu-id="5a77a-384">1253</span><span class="sxs-lookup"><span data-stu-id="5a77a-384">1253</span></span>    | <span data-ttu-id="5a77a-385">04E5</span><span class="sxs-lookup"><span data-stu-id="5a77a-385">04E5</span></span>        | <span data-ttu-id="5a77a-386">Греческий</span><span class="sxs-lookup"><span data-stu-id="5a77a-386">Greek</span></span>                      |
| <span data-ttu-id="5a77a-387">1254</span><span class="sxs-lookup"><span data-stu-id="5a77a-387">1254</span></span>    | <span data-ttu-id="5a77a-388">04E6</span><span class="sxs-lookup"><span data-stu-id="5a77a-388">04E6</span></span>        | <span data-ttu-id="5a77a-389">Турецкий</span><span class="sxs-lookup"><span data-stu-id="5a77a-389">Turkish</span></span>                    |
| <span data-ttu-id="5a77a-390">1255</span><span class="sxs-lookup"><span data-stu-id="5a77a-390">1255</span></span>    | <span data-ttu-id="5a77a-391">04E7</span><span class="sxs-lookup"><span data-stu-id="5a77a-391">04E7</span></span>        | <span data-ttu-id="5a77a-392">Иврит</span><span class="sxs-lookup"><span data-stu-id="5a77a-392">Hebrew</span></span>                     |
| <span data-ttu-id="5a77a-393">1256</span><span class="sxs-lookup"><span data-stu-id="5a77a-393">1256</span></span>    | <span data-ttu-id="5a77a-394">04E8</span><span class="sxs-lookup"><span data-stu-id="5a77a-394">04E8</span></span>        | <span data-ttu-id="5a77a-395">Арабский</span><span class="sxs-lookup"><span data-stu-id="5a77a-395">Arabic</span></span>                     |



 

</dd> <dt>

<span data-ttu-id="5a77a-396"><span id="string-name"></span><span id="STRING-NAME"></span>*строка-имя*</span><span class="sxs-lookup"><span data-stu-id="5a77a-396"><span id="string-name"></span><span id="STRING-NAME"></span>*string-name*</span></span>
</dt> <dd>

<span data-ttu-id="5a77a-397">Одно из следующих предопределенных имен.</span><span class="sxs-lookup"><span data-stu-id="5a77a-397">One of the following predefined names.</span></span>



| <span data-ttu-id="5a77a-398">Имя</span><span class="sxs-lookup"><span data-stu-id="5a77a-398">Name</span></span>                 | <span data-ttu-id="5a77a-399">Описание</span><span class="sxs-lookup"><span data-stu-id="5a77a-399">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a77a-400">**Комментарии**</span><span class="sxs-lookup"><span data-stu-id="5a77a-400">**Comments**</span></span>         | <span data-ttu-id="5a77a-401">Дополнительные сведения, которые должны отображаться в целях диагностики.</span><span class="sxs-lookup"><span data-stu-id="5a77a-401">Additional information that should be displayed for diagnostic purposes.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="5a77a-402">**Название**</span><span class="sxs-lookup"><span data-stu-id="5a77a-402">**CompanyName**</span></span>      | <span data-ttu-id="5a77a-403">Компания, создавшая файл? например, "Корпорация Майкрософт" или "Стандартный Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="5a77a-403">Company that produced the file?for example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span> <span data-ttu-id="5a77a-404">Эта строка является обязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-404">This string is required.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="5a77a-405">**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="5a77a-405">**FileDescription**</span></span>  | <span data-ttu-id="5a77a-406">Описание файла, которое будет представлено пользователям.</span><span class="sxs-lookup"><span data-stu-id="5a77a-406">File description to be presented to users.</span></span> <span data-ttu-id="5a77a-407">Эта строка может отображаться в списке, когда пользователь выбирает файлы для установки? например, "драйвер клавиатуры для AT-Style клавиатуры".</span><span class="sxs-lookup"><span data-stu-id="5a77a-407">This string may be displayed in a list box when the user is choosing files to install?for example, "Keyboard Driver for AT-Style Keyboards".</span></span> <span data-ttu-id="5a77a-408">Эта строка является обязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-408">This string is required.</span></span>                                                                                            |
| <span data-ttu-id="5a77a-409">**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="5a77a-409">**FileVersion**</span></span>      | <span data-ttu-id="5a77a-410">Номер версии файла? например, "3,10" или "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="5a77a-410">Version number of the file?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="5a77a-411">Эта строка является обязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-411">This string is required.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="5a77a-412">**InternalName**</span><span class="sxs-lookup"><span data-stu-id="5a77a-412">**InternalName**</span></span>     | <span data-ttu-id="5a77a-413">Внутреннее имя файла, если оно существует? например, имя модуля, если файл является библиотекой динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="5a77a-413">Internal name of the file, if one exists?for example, a module name if the file is a dynamic-link library.</span></span> <span data-ttu-id="5a77a-414">Если у файла нет внутреннего имени, эта строка должна быть исходным именем файла без расширения.</span><span class="sxs-lookup"><span data-stu-id="5a77a-414">If the file has no internal name, this string should be the original filename, without extension.</span></span> <span data-ttu-id="5a77a-415">Эта строка является обязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-415">This string is required.</span></span>                                                                       |
| <span data-ttu-id="5a77a-416">**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="5a77a-416">**LegalCopyright**</span></span>   | <span data-ttu-id="5a77a-417">Уведомления об авторских правах, применимые к файлу.</span><span class="sxs-lookup"><span data-stu-id="5a77a-417">Copyright notices that apply to the file.</span></span> <span data-ttu-id="5a77a-418">Это должен быть полный текст всех уведомлений, допустимых символов, дат авторских прав и т. д.</span><span class="sxs-lookup"><span data-stu-id="5a77a-418">This should include the full text of all notices, legal symbols, copyright dates, and so on.</span></span> <span data-ttu-id="5a77a-419">Эта строка является необязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-419">This string is optional.</span></span>                                                                                                                                             |
| <span data-ttu-id="5a77a-420">**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="5a77a-420">**LegalTrademarks**</span></span>  | <span data-ttu-id="5a77a-421">Товарные знаки и охраняемые товарные знаки, которые применяются к файлу.</span><span class="sxs-lookup"><span data-stu-id="5a77a-421">Trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="5a77a-422">Это должен быть полный текст всех уведомлений, допустимых символов, номера товарных знаков и так далее.</span><span class="sxs-lookup"><span data-stu-id="5a77a-422">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="5a77a-423">Эта строка является необязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-423">This string is optional.</span></span>                                                                                                                        |
| <span data-ttu-id="5a77a-424">**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="5a77a-424">**OriginalFilename**</span></span> | <span data-ttu-id="5a77a-425">Исходное имя файла, не включая путь.</span><span class="sxs-lookup"><span data-stu-id="5a77a-425">Original name of the file, not including a path.</span></span> <span data-ttu-id="5a77a-426">Эта информация позволяет приложению определить, был ли файл переименован пользователем.</span><span class="sxs-lookup"><span data-stu-id="5a77a-426">This information enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="5a77a-427">Формат имени зависит от файловой системы, для которой был создан файл.</span><span class="sxs-lookup"><span data-stu-id="5a77a-427">The format of the name depends on the file system for which the file was created.</span></span> <span data-ttu-id="5a77a-428">Эта строка является обязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-428">This string is required.</span></span>                                                 |
| <span data-ttu-id="5a77a-429">**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="5a77a-429">**PrivateBuild**</span></span>     | <span data-ttu-id="5a77a-430">Сведения о закрытой версии файла, например "строится by TESTER1 On \\ экспериментальные".</span><span class="sxs-lookup"><span data-stu-id="5a77a-430">Information about a private version of the file?for example, "Built by TESTER1 on \\TESTBED".</span></span> <span data-ttu-id="5a77a-431">Эта строка должна присутствовать, только если в параметре *раздела FILEFLAGS* корневого блока указано **VS \_ FF \_ приватебуилд** .</span><span class="sxs-lookup"><span data-stu-id="5a77a-431">This string should be present only if **VS\_FF\_PRIVATEBUILD** is specified in the *fileflags* parameter of the root block.</span></span>                                                                                   |
| <span data-ttu-id="5a77a-432">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="5a77a-432">**ProductName**</span></span>      | <span data-ttu-id="5a77a-433">Имя продукта, с которым распространяется файл.</span><span class="sxs-lookup"><span data-stu-id="5a77a-433">Name of the product with which the file is distributed.</span></span> <span data-ttu-id="5a77a-434">Эта строка является обязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-434">This string is required.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="5a77a-435">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="5a77a-435">**ProductVersion**</span></span>   | <span data-ttu-id="5a77a-436">Версия продукта, с которой распространяется файл? например, "3,10" или "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="5a77a-436">Version of the product with which the file is distributed?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="5a77a-437">Эта строка является обязательной.</span><span class="sxs-lookup"><span data-stu-id="5a77a-437">This string is required.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="5a77a-438">**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="5a77a-438">**SpecialBuild**</span></span>     | <span data-ttu-id="5a77a-439">Текст, указывающий, как эта версия файла отличается от стандартной версии? например, "частная сборка для TESTER1. решение проблем мыши на компьютерах M250 и M250E".</span><span class="sxs-lookup"><span data-stu-id="5a77a-439">Text that indicates how this version of the file differs from the standard version?for example, "Private build for TESTER1 solving mouse problems on M250 and M250E computers".</span></span> <span data-ttu-id="5a77a-440">Эта строка должна присутствовать, только если в параметре *раздела FILEFLAGS* корневого блока указано **VS \_ FF \_ спеЦиалбуилд** .</span><span class="sxs-lookup"><span data-stu-id="5a77a-440">This string should be present only if **VS\_FF\_SPECIALBUILD** is specified in the *fileflags* parameter of the root block.</span></span> |



 

</dd> </dl>

<span data-ttu-id="5a77a-441">Для обратной совместимости также поддерживаются некоторые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="5a77a-441">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="5a77a-442">Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="5a77a-442">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5a77a-443">Примеры</span><span class="sxs-lookup"><span data-stu-id="5a77a-443">Examples</span></span>

<span data-ttu-id="5a77a-444">В следующем примере определяется ресурс **versionInfo** :</span><span class="sxs-lookup"><span data-stu-id="5a77a-444">The following example defines a **VERSIONINFO** resource:</span></span>

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a><span data-ttu-id="5a77a-445">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a77a-445">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a77a-446">Использование сведений о версии</span><span class="sxs-lookup"><span data-stu-id="5a77a-446">Using Version Information</span></span>](./using-version-information.md)
</dt> <dt>

[<span data-ttu-id="5a77a-447">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="5a77a-447">Version Information</span></span>](./version-information.md)
</dt> </dl>

 

 