---
title: Структура строки
description: Представляет организацию данных в ресурсе версии файла. Он содержит строку, описывающую конкретный аспект файла, например версию файла, уведомления об авторских правах или его товарные знаки.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Меню структуры строк и другие ресурсы
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691790"
---
# <a name="string-structure"></a><span data-ttu-id="1669c-105">Структура строки</span><span class="sxs-lookup"><span data-stu-id="1669c-105">String structure</span></span>

<span data-ttu-id="1669c-106">Представляет организацию данных в ресурсе версии файла.</span><span class="sxs-lookup"><span data-stu-id="1669c-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="1669c-107">Он содержит строку, описывающую конкретный аспект файла, например версию файла, уведомления об авторских правах или его товарные знаки.</span><span class="sxs-lookup"><span data-stu-id="1669c-107">It contains a string that describes a specific aspect of a file, for example, a file's version, its copyright notices, or its trademarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="1669c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1669c-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a><span data-ttu-id="1669c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1669c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1669c-110">**вленгс**</span><span class="sxs-lookup"><span data-stu-id="1669c-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="1669c-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="1669c-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1669c-112">Длина данной структуры **строки** в байтах.</span><span class="sxs-lookup"><span data-stu-id="1669c-112">The length, in bytes, of this **String** structure.</span></span>

</dd> <dt>

<span data-ttu-id="1669c-113">**ввалуеленгс**</span><span class="sxs-lookup"><span data-stu-id="1669c-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="1669c-114">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="1669c-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1669c-115">Размер (в словах) элемента **value** .</span><span class="sxs-lookup"><span data-stu-id="1669c-115">The size, in words, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="1669c-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="1669c-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="1669c-117">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="1669c-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1669c-118">Тип данных в ресурсе версии.</span><span class="sxs-lookup"><span data-stu-id="1669c-118">The type of data in the version resource.</span></span> <span data-ttu-id="1669c-119">Этот элемент равен 1, если ресурс версии содержит текстовые данные, и 0, если ресурс версии содержит двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="1669c-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="1669c-120">**сзкэй**</span><span class="sxs-lookup"><span data-stu-id="1669c-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="1669c-121">Тип: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="1669c-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="1669c-122">Произвольная строка в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1669c-122">An arbitrary Unicode string.</span></span> <span data-ttu-id="1669c-123">Элемент **сзкэй** может иметь одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1669c-123">The **szKey** member can be one or more of the following values.</span></span> <span data-ttu-id="1669c-124">Эти значения являются рекомендациями.</span><span class="sxs-lookup"><span data-stu-id="1669c-124">These values are guidelines only.</span></span>

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span data-ttu-id="1669c-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Обсуждения**</span><span class="sxs-lookup"><span data-stu-id="1669c-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comments**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-126">Элемент **value** содержит любые дополнительные сведения, которые должны отображаться в целях диагностики.</span><span class="sxs-lookup"><span data-stu-id="1669c-126">The **Value** member contains any additional information that should be displayed for diagnostic purposes.</span></span> <span data-ttu-id="1669c-127">Эта строка может иметь произвольную длину.</span><span class="sxs-lookup"><span data-stu-id="1669c-127">This string can be an arbitrary length.</span></span>

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span data-ttu-id="1669c-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Название**</span><span class="sxs-lookup"><span data-stu-id="1669c-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-129">Элемент **значение** определяет компанию, которая создала файл.</span><span class="sxs-lookup"><span data-stu-id="1669c-129">The **Value** member identifies the company that produced the file.</span></span> <span data-ttu-id="1669c-130">Например, "Корпорация Майкрософт" или "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="1669c-130">For example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span>

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span data-ttu-id="1669c-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**филедескриптион**</span><span class="sxs-lookup"><span data-stu-id="1669c-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-132">Элемент **value** описывает файл таким образом, чтобы его можно было представить пользователям.</span><span class="sxs-lookup"><span data-stu-id="1669c-132">The **Value** member describes the file in such a way that it can be presented to users.</span></span> <span data-ttu-id="1669c-133">Эта строка может быть представлена в списке, когда пользователь выбирает файлы для установки.</span><span class="sxs-lookup"><span data-stu-id="1669c-133">This string may be presented in a list box when the user is choosing files to install.</span></span> <span data-ttu-id="1669c-134">Например, "драйвер клавиатуры для клавиатуры в стиле" или "Microsoft Word для Windows".</span><span class="sxs-lookup"><span data-stu-id="1669c-134">For example, "Keyboard driver for AT-style keyboards" or "Microsoft Word for Windows".</span></span>

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span data-ttu-id="1669c-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="1669c-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-136">Элемент **value** определяет версию этого файла.</span><span class="sxs-lookup"><span data-stu-id="1669c-136">The **Value** member identifies the version of this file.</span></span> <span data-ttu-id="1669c-137">Например, **значение** может быть "3.00 a" или "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="1669c-137">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span data-ttu-id="1669c-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**интерналнаме**</span><span class="sxs-lookup"><span data-stu-id="1669c-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-139">Член **value** определяет внутреннее имя файла, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="1669c-139">The **Value** member identifies the file's internal name, if one exists.</span></span> <span data-ttu-id="1669c-140">Например, эта строка может содержать имя модуля для библиотеки DLL, имя виртуального устройства для виртуального устройства Windows или имя устройства для драйвера устройства MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="1669c-140">For example, this string could contain the module name for a DLL, a virtual device name for a Windows virtual device, or a device name for a MS-DOS device driver.</span></span>

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span data-ttu-id="1669c-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**легалкопиригхт**</span><span class="sxs-lookup"><span data-stu-id="1669c-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-142">Элемент **value** описывает все уведомления об авторских правах, товарные знаки и зарегистрированные товарные знаки, которые применяются к файлу.</span><span class="sxs-lookup"><span data-stu-id="1669c-142">The **Value** member describes all copyright notices, trademarks, and registered trademarks that apply to the file.</span></span> <span data-ttu-id="1669c-143">Это должен быть полный текст всех уведомлений, допустимых символов, сроки действия прав, номера товарных знаков и так далее.</span><span class="sxs-lookup"><span data-stu-id="1669c-143">This should include the full text of all notices, legal symbols, copyright dates, trademark numbers, and so on.</span></span> <span data-ttu-id="1669c-144">На английском языке эта строка должна иметь формат "© Microsoft Corp. 1990 1994".</span><span class="sxs-lookup"><span data-stu-id="1669c-144">In English, this string should be in the format "Copyright Microsoft Corp. 1990  1994".</span></span>

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span data-ttu-id="1669c-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**легалтрадемаркс**</span><span class="sxs-lookup"><span data-stu-id="1669c-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-146">Элемент **значение** описывает все товарные знаки и зарегистрированные товарные знаки, которые применяются к файлу.</span><span class="sxs-lookup"><span data-stu-id="1669c-146">The **Value** member describes all trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="1669c-147">Это должен быть полный текст всех уведомлений, допустимых символов, номера товарных знаков и так далее.</span><span class="sxs-lookup"><span data-stu-id="1669c-147">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="1669c-148">На русском языке эта строка должна быть в формате "Windows является товарным знаком корпорации Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="1669c-148">In English, this string should be in the format "Windows is a trademark of Microsoft Corporation".</span></span>

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span data-ttu-id="1669c-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**оригиналфиленаме**</span><span class="sxs-lookup"><span data-stu-id="1669c-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-150">Элемент **value** определяет исходное имя файла, не включая путь.</span><span class="sxs-lookup"><span data-stu-id="1669c-150">The **Value** member identifies the original name of the file, not including a path.</span></span> <span data-ttu-id="1669c-151">Это позволяет приложению определить, был ли файл переименован пользователем.</span><span class="sxs-lookup"><span data-stu-id="1669c-151">This enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="1669c-152">Это имя может быть не в формате MS-DOS 8,3-Format, если файл относится только к файловой системе, отличной от FAT.</span><span class="sxs-lookup"><span data-stu-id="1669c-152">This name may not be MS-DOS 8.3-format if the file is specific to a non-FAT file system.</span></span>

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span data-ttu-id="1669c-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**приватебуилд**</span><span class="sxs-lookup"><span data-stu-id="1669c-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-154">Элемент **value** описывает, кем, где и почему была создана эта частная версия файла.</span><span class="sxs-lookup"><span data-stu-id="1669c-154">The **Value** member describes by whom, where, and why this private version of the file was built.</span></span> <span data-ttu-id="1669c-155">Эта строка должна присутствовать только в том случае, если флаг **VS \_ FF \_ приватебуилд** установлен в элементе **двфилефлагс** структуры [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="1669c-155">This string should only be present if the **VS\_FF\_PRIVATEBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="1669c-156">Например, **значение** может быть "построено с помощью интерфейса OSCAR в \\ OSCAR2".</span><span class="sxs-lookup"><span data-stu-id="1669c-156">For example, **Value** could be "Built by OSCAR on \\OSCAR2".</span></span>

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span data-ttu-id="1669c-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span><span class="sxs-lookup"><span data-stu-id="1669c-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-158">Элемент **value** определяет имя продукта, с которым распространяется этот файл.</span><span class="sxs-lookup"><span data-stu-id="1669c-158">The **Value** member identifies the name of the product with which this file is distributed.</span></span> <span data-ttu-id="1669c-159">Например, эта строка может иметь значение "Microsoft Windows".</span><span class="sxs-lookup"><span data-stu-id="1669c-159">For example, this string could be "Microsoft Windows".</span></span>

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span data-ttu-id="1669c-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="1669c-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-161">Элемент **value** определяет версию продукта, с которым распространяется этот файл.</span><span class="sxs-lookup"><span data-stu-id="1669c-161">The **Value** member identifies the version of the product with which this file is distributed.</span></span> <span data-ttu-id="1669c-162">Например, **значение** может быть "3.00 a" или "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="1669c-162">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span data-ttu-id="1669c-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**спеЦиалбуилд**</span><span class="sxs-lookup"><span data-stu-id="1669c-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span></span>


</dt> <dd>

<span data-ttu-id="1669c-164">Элемент **value** описывает, чем эта версия файла отличается от обычной версии.</span><span class="sxs-lookup"><span data-stu-id="1669c-164">The **Value** member describes how this version of the file differs from the normal version.</span></span> <span data-ttu-id="1669c-165">Эта запись должна присутствовать только в том случае, если флаг **VS \_ FF \_ спеЦиалбуилд** установлен в элементе **двфилефлагс** структуры [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="1669c-165">This entry should only be present if the **VS\_FF\_SPECIALBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="1669c-166">Например, **значение** может быть "частная сборка для проблем с мышью для решения Olivetti на компьютерах M250 и M250E".</span><span class="sxs-lookup"><span data-stu-id="1669c-166">For example, **Value** could be "Private build for Olivetti solving mouse problems on M250 and M250E computers".</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1669c-167">**Заполнение**</span><span class="sxs-lookup"><span data-stu-id="1669c-167">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="1669c-168">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="1669c-168">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1669c-169">Столько нуля слов, сколько необходимо, чтобы вычислить **значение** элемента на 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="1669c-169">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="1669c-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1669c-170">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="1669c-171">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="1669c-171">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1669c-172">Строка, завершающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="1669c-172">A zero-terminated string.</span></span> <span data-ttu-id="1669c-173">Дополнительные сведения см. в описании члена **сзкэй** .</span><span class="sxs-lookup"><span data-stu-id="1669c-173">See the **szKey** member description for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1669c-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1669c-174">Remarks</span></span>

<span data-ttu-id="1669c-175">Эта структура не является истинной структурой языка C, так как она содержит члены переменной длины.</span><span class="sxs-lookup"><span data-stu-id="1669c-175">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="1669c-176">Эта структура была создана только для описания организации данных в ресурсе версии и не отображается ни в одном из файлов заголовков, поставляемых вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="1669c-176">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="1669c-177">Структура **строки** может иметь значение **сзкэй** , например "CompanyName", и **значение** "Корпорация Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="1669c-177">A **String** structure may have an **szKey** value of, for example, "CompanyName" and a **Value** of "Microsoft Corporation".</span></span> <span data-ttu-id="1669c-178">Другая структура **строки** с тем же значением **Сзкэй** может содержать **значение** "Microsoft GmbH".</span><span class="sxs-lookup"><span data-stu-id="1669c-178">Another **String** structure with the same **szKey** value could contain a **Value** of "Microsoft GmbH".</span></span> <span data-ttu-id="1669c-179">Это может произойти, если вторая **строка** была связана со структурой [**STRINGTABLE**](stringtable.md) , **сзкэй** значение которой равно 040704B0, то есть немецкий/Unicode.</span><span class="sxs-lookup"><span data-stu-id="1669c-179">This might occur if the second **String** structure were associated with a [**StringTable**](stringtable.md) structure whose **szKey** value is 040704b0   that is, German/Unicode.</span></span>

## <a name="requirements"></a><span data-ttu-id="1669c-180">Требования</span><span class="sxs-lookup"><span data-stu-id="1669c-180">Requirements</span></span>



| <span data-ttu-id="1669c-181">Требование</span><span class="sxs-lookup"><span data-stu-id="1669c-181">Requirement</span></span> | <span data-ttu-id="1669c-182">Значение</span><span class="sxs-lookup"><span data-stu-id="1669c-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1669c-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1669c-183">Minimum supported client</span></span><br/> | <span data-ttu-id="1669c-184">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1669c-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1669c-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1669c-185">Minimum supported server</span></span><br/> | <span data-ttu-id="1669c-186">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1669c-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1669c-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1669c-187">See also</span></span>

<dl> <dt>

<span data-ttu-id="1669c-188">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1669c-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1669c-189">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="1669c-189">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="1669c-190">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="1669c-190">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[<span data-ttu-id="1669c-191">**стрингфилеинфо**</span><span class="sxs-lookup"><span data-stu-id="1669c-191">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="1669c-192">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="1669c-192">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="1669c-193">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1669c-193">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1669c-194">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="1669c-194">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





