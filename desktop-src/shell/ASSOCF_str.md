---
description: Предоставляет сведения для методов интерфейса ИкуеряссоЦиатионс.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Перечисление АССОКФ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273309"
---
# <a name="assocf-enumeration"></a><span data-ttu-id="93b56-103">Перечисление АССОКФ</span><span class="sxs-lookup"><span data-stu-id="93b56-103">ASSOCF enumeration</span></span>

<span data-ttu-id="93b56-104">Предоставляет сведения для методов интерфейса [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="93b56-104">Provides information to the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="93b56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93b56-105">Syntax</span></span>

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="93b56-106">C++</span><span class="sxs-lookup"><span data-stu-id="93b56-106">C++</span></span></th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a><span data-ttu-id="93b56-107">Константы</span><span class="sxs-lookup"><span data-stu-id="93b56-107">Constants</span></span>

 <span data-ttu-id="93b56-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**АССОКФ \_ None**</span><span class="sxs-lookup"><span data-stu-id="93b56-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF\_NONE**</span></span> 

<span data-ttu-id="93b56-109">Не задан ни один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="93b56-109">None of the following options are set.</span></span>

 <span data-ttu-id="93b56-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**АССОКФ \_ init \_ норемапклсид**</span><span class="sxs-lookup"><span data-stu-id="93b56-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF\_INIT\_NOREMAPCLSID**</span></span> 

<span data-ttu-id="93b56-111">Указывает, что методы интерфейса [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не СОПОСТАВЛЯЮТ значения CLSID со значениями ProgID.</span><span class="sxs-lookup"><span data-stu-id="93b56-111">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods not to map CLSID values to ProgID values.</span></span>

 <span data-ttu-id="93b56-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**АССОКФ \_ init \_ бексенаме**</span><span class="sxs-lookup"><span data-stu-id="93b56-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF\_INIT\_BYEXENAME**</span></span> 

<span data-ttu-id="93b56-113">Определяет значение параметра *Пвсзассок* [**ИкуеряссоЦиатионс:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) в качестве имени исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="93b56-113">Identifies the value of the *pwszAssoc* parameter of [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) as an executable file name.</span></span> <span data-ttu-id="93b56-114">Если этот флаг не установлен, для корневого ключа будет задан идентификатор ProgID, связанный с ключом **exe** , а не исполняемый файл ProgID.</span><span class="sxs-lookup"><span data-stu-id="93b56-114">If this flag is not set, the root key will be set to the ProgID associated with the **.exe** key instead of the executable file's ProgID.</span></span>

 <span data-ttu-id="93b56-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**АССОКФ \_ Open \_ бексенаме**</span><span class="sxs-lookup"><span data-stu-id="93b56-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF\_OPEN\_BYEXENAME**</span></span> 

<span data-ttu-id="93b56-116">Идентично **ассокф \_ init \_ бексенаме**.</span><span class="sxs-lookup"><span data-stu-id="93b56-116">Identical to **ASSOCF\_INIT\_BYEXENAME**.</span></span>

 <span data-ttu-id="93b56-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**АССОКФ \_ init \_ дефаулттостар**</span><span class="sxs-lookup"><span data-stu-id="93b56-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF\_INIT\_DEFAULTTOSTAR**</span></span> 

<span data-ttu-id="93b56-118">Указывает, что когда метод [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не находит запрошенное значение в корневом ключе, он должен попытаться получить сравниваемое значение из **\*** подраздела.</span><span class="sxs-lookup"><span data-stu-id="93b56-118">Specifies that when an [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **\*** subkey.</span></span>

 <span data-ttu-id="93b56-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**АССОКФ \_ init \_ дефаулттофолдер**</span><span class="sxs-lookup"><span data-stu-id="93b56-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF\_INIT\_DEFAULTTOFOLDER**</span></span> 

<span data-ttu-id="93b56-120">Указывает, что когда метод [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не находит запрошенное значение в корневом ключе, он должен попытаться получить сравниваемое значение из подраздела **Folder** .</span><span class="sxs-lookup"><span data-stu-id="93b56-120">Specifies that when a [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **Folder** subkey.</span></span>

 <span data-ttu-id="93b56-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**АССОКФ \_ наусерсеттингс**</span><span class="sxs-lookup"><span data-stu-id="93b56-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF\_NOUSERSETTINGS**</span></span> 

<span data-ttu-id="93b56-122">Указывает, что должен быть выполнен поиск только **\_ \_ корневых классов hKey** , и **\_ текущий \_ пользователь hKey** должен игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="93b56-122">Specifies that only **HKEY\_CLASSES\_ROOT** should be searched, and that **HKEY\_CURRENT\_USER** should be ignored.</span></span>

 <span data-ttu-id="93b56-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**АССОКФ \_ усечение**</span><span class="sxs-lookup"><span data-stu-id="93b56-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF\_NOTRUNCATE**</span></span> 

<span data-ttu-id="93b56-124">Указывает, что возвращаемая строка не должна быть усечена.</span><span class="sxs-lookup"><span data-stu-id="93b56-124">Specifies that the return string should not be truncated.</span></span> <span data-ttu-id="93b56-125">Вместо этого следует возвращать значение ошибки и необходимый размер для полной строки.</span><span class="sxs-lookup"><span data-stu-id="93b56-125">Instead, return an error value and the required size for the complete string.</span></span>

 <span data-ttu-id="93b56-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**\_Проверка ассокф**</span><span class="sxs-lookup"><span data-stu-id="93b56-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF\_VERIFY**</span></span> 

<span data-ttu-id="93b56-127">Инструктирует методы [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) для проверки правильности данных.</span><span class="sxs-lookup"><span data-stu-id="93b56-127">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to verify that data is accurate.</span></span> <span data-ttu-id="93b56-128">Этот параметр позволяет методам **икуеряссоЦиатионс** считывать данные с жесткого диска пользователя для проверки.</span><span class="sxs-lookup"><span data-stu-id="93b56-128">This setting allows **IQueryAssociations** methods to read data from the user's hard disk for verification.</span></span> <span data-ttu-id="93b56-129">Например, они могут проверить понятное имя в реестре на соответствие сохраненному в exe файле.</span><span class="sxs-lookup"><span data-stu-id="93b56-129">For example, they can check the friendly name in the registry against the one stored in the .exe file.</span></span> <span data-ttu-id="93b56-130">Установка этого флага обычно сокращает эффективность метода.</span><span class="sxs-lookup"><span data-stu-id="93b56-130">Setting this flag typically reduces the efficiency of the method.</span></span>

 <span data-ttu-id="93b56-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**АССОКФ \_ ремапрундлл**</span><span class="sxs-lookup"><span data-stu-id="93b56-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF\_REMAPRUNDLL**</span></span> 

<span data-ttu-id="93b56-132">Указывает, что методы [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не пропускают Rundll.exe и возвращают сведения о ее целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="93b56-132">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to ignore Rundll.exe and return information about its target.</span></span> <span data-ttu-id="93b56-133">Обычно методы **икуеряссоЦиатионс** возвращают сведения о первом exe-или DLL в командной строке.</span><span class="sxs-lookup"><span data-stu-id="93b56-133">Typically **IQueryAssociations** methods return information about the first .exe or .dll in a command string.</span></span> <span data-ttu-id="93b56-134">Если команда использует Rundll.exe, установка этого флага указывает методу игнорировать Rundll.exe и возвращать сведения о целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="93b56-134">If a command uses Rundll.exe, setting this flag tells the method to ignore Rundll.exe and return information about its target.</span></span>

 <span data-ttu-id="93b56-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**АССОКФные \_ исправления**</span><span class="sxs-lookup"><span data-stu-id="93b56-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF\_NOFIXUPS**</span></span> 

<span data-ttu-id="93b56-136">Указывает методам [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) не исправлять ошибки в реестре, например понятное имя функции, не совпадающее с именем, найденным в exe-файле.</span><span class="sxs-lookup"><span data-stu-id="93b56-136">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods not to fix errors in the registry, such as the friendly name of a function not matching the one found in the .exe file.</span></span>

 <span data-ttu-id="93b56-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**АССОКФ \_ игноребасекласс**</span><span class="sxs-lookup"><span data-stu-id="93b56-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF\_IGNOREBASECLASS**</span></span> 

<span data-ttu-id="93b56-138">Указывает, что значение BaseClass следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="93b56-138">Specifies that the BaseClass value should be ignored.</span></span>

 <span data-ttu-id="93b56-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**АССОКФ \_ init \_ игнореункновн**</span><span class="sxs-lookup"><span data-stu-id="93b56-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF\_INIT\_IGNOREUNKNOWN**</span></span> 

<span data-ttu-id="93b56-140">**Впервые появился в Windows 7**.</span><span class="sxs-lookup"><span data-stu-id="93b56-140">**Introduced in Windows 7**.</span></span> <span data-ttu-id="93b56-141">Указывает, что ProgID "Unknown" следует игнорировать. Вместо этого происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="93b56-141">Specifies that the "Unknown" ProgID should be ignored; instead, fail.</span></span>

 <span data-ttu-id="93b56-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**\_ \_ фиксированный \_ идентификатор ProgID ассокф init**</span><span class="sxs-lookup"><span data-stu-id="93b56-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF\_INIT\_FIXED\_PROGID**</span></span> 

<span data-ttu-id="93b56-143">**Впервые появился в Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="93b56-143">**Introduced in Windows 8**.</span></span> <span data-ttu-id="93b56-144">Указывает, что указанный идентификатор ProgID должен быть сопоставлен с использованием системных значений по умолчанию, а не по умолчанию текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="93b56-144">Specifies that the supplied ProgID should be mapped using the system defaults, rather than the current user defaults.</span></span>

 <span data-ttu-id="93b56-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**АССОКФ \_ — \_ протокол**</span><span class="sxs-lookup"><span data-stu-id="93b56-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF\_IS\_PROTOCOL**</span></span> 

<span data-ttu-id="93b56-146">**Впервые появился в Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="93b56-146">**Introduced in Windows 8**.</span></span> <span data-ttu-id="93b56-147">Указывает, что значение является протоколом и должно быть сопоставлено с текущими значениями по умолчанию для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="93b56-147">Specifies that the value is a protocol, and should be mapped using the current user defaults.</span></span>

 <span data-ttu-id="93b56-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**\_Инициализация ассокф \_ для \_ файла**</span><span class="sxs-lookup"><span data-stu-id="93b56-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF\_INIT\_FOR\_FILE**</span></span> 

<span data-ttu-id="93b56-149">**Введено в Windows 8.1**.</span><span class="sxs-lookup"><span data-stu-id="93b56-149">**Introduced in Windows 8.1**.</span></span> <span data-ttu-id="93b56-150">Указывает, что идентификатор ProgID соответствует сопоставлению на основе расширения файла.</span><span class="sxs-lookup"><span data-stu-id="93b56-150">Specifies that the ProgID corresponds with a file extension based association.</span></span> <span data-ttu-id="93b56-151">Используйте совместно с **\_ \_ фиксированным \_ идентификатором ProgID ассокф init**.</span><span class="sxs-lookup"><span data-stu-id="93b56-151">Use together with **ASSOCF\_INIT\_FIXED\_PROGID**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="93b56-152">Требования</span><span class="sxs-lookup"><span data-stu-id="93b56-152">Requirements</span></span>



| <span data-ttu-id="93b56-153">Требование</span><span class="sxs-lookup"><span data-stu-id="93b56-153">Requirement</span></span> | <span data-ttu-id="93b56-154">Значение</span><span class="sxs-lookup"><span data-stu-id="93b56-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93b56-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93b56-155">Minimum supported client</span></span> | <span data-ttu-id="93b56-156">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93b56-156">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span>               |
| <span data-ttu-id="93b56-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93b56-157">Minimum supported server</span></span> | <span data-ttu-id="93b56-158">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="93b56-158">Windows 2000 Server \[desktop apps only\]</span></span>                                 |
| <span data-ttu-id="93b56-159">Заголовок</span><span class="sxs-lookup"><span data-stu-id="93b56-159">Header</span></span>                   |  <span data-ttu-id="93b56-160">Shlwapi. h</span><span class="sxs-lookup"><span data-stu-id="93b56-160">Shlwapi.h</span></span>  |



## <a name="see-also"></a><span data-ttu-id="93b56-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93b56-161">See also</span></span>

 <span data-ttu-id="93b56-162">[**Ассоккуерикэй**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**ассоккуеристринг**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**ассоккуеристрингбикэй**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span><span class="sxs-lookup"><span data-stu-id="93b56-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span></span> 

 

 

<span data-ttu-id="93b56-163">© Майкрософт (Microsoft), 2017.</span><span class="sxs-lookup"><span data-stu-id="93b56-163">© 2017 Microsoft.</span></span> <span data-ttu-id="93b56-164">Все права защищены.</span><span class="sxs-lookup"><span data-stu-id="93b56-164">All rights reserved.</span></span>
