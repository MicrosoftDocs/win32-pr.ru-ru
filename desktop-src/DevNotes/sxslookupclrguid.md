---
description: Извлекает имя класса и другие сведения, связанные с данным идентификатором GUID в манифесте компонента.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: Функция Сксслукупклргуид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648071"
---
# <a name="sxslookupclrguid-function"></a><span data-ttu-id="b1722-103">Функция Сксслукупклргуид</span><span class="sxs-lookup"><span data-stu-id="b1722-103">SxsLookupClrGuid function</span></span>

<span data-ttu-id="b1722-104">Извлекает имя класса и другие сведения, связанные с данным идентификатором GUID в манифесте компонента.</span><span class="sxs-lookup"><span data-stu-id="b1722-104">Retrieves the class name and other information associated with a given GUID in a component's manifest.</span></span> <span data-ttu-id="b1722-105">Эта функция используется только при реализации низкоуровневого управляемого неуправляемого взаимодействия в платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b1722-105">This function is used only when implementing low-level managed-unmanaged interoperability in the .NET Framework.</span></span> <span data-ttu-id="b1722-106">Дополнительные сведения о взаимодействии управляемого и неуправляемого кода см. в разделе "взаимодействие с неуправляемым кодом" раздела платформа .NET Framework SDK, а также [изолированные приложения и параллельные сборки](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b1722-106">For more information about managed-unmanaged interoperability, see "Interoperating with Unmanaged Code" in the .NET Framework SDK and also [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1722-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1722-107">Syntax</span></span>


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b1722-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1722-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1722-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1722-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1722-110">Сочетание следующих флагов (ноль или более).</span><span class="sxs-lookup"><span data-stu-id="b1722-110">A combination of zero or more of the following flags.</span></span>



| <span data-ttu-id="b1722-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b1722-111">Value</span></span>                                                                                                                                                                                                                                                                                             | <span data-ttu-id="b1722-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b1722-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <span data-ttu-id="b1722-113"><dt>**SxS \_ УТОЧНЯющий запрос \_ CLR \_ GUID \_ USE \_ акткткс**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b1722-113"><dt>**SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX**</dt> <dt>0x00000001</dt></span></span> </dl>              | <span data-ttu-id="b1722-114">Если этот флаг установлен, параметр *хакткткс* должен содержать обработчик контекста активации, возвращаемый функцией [**креатеакткткс**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="b1722-114">If this flag is set, then the *hActCtx* parameter must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="b1722-115">Если этот флаг не установлен, параметр *хакткткс* игнорируется и **сксслукупклргуид** ищет активный в данный момент контекст активации (функция [**активатеакткткс**](/windows/win32/api/winbase/nf-winbase-activateactctx) используется, чтобы активировать контекст активации).</span><span class="sxs-lookup"><span data-stu-id="b1722-115">If this flag is not set, the *hActCtx* parameter is ignored and **SxsLookupClrGuid** searches the activation context that is currently active (the [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) function is used to make an activation context active).</span></span><br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <span data-ttu-id="b1722-116"><dt>**SxS \_ УТОЧНЯющий запрос GUID поиска- \_ \_ идентификатора \_ \_ CLR**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="b1722-116"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE**</dt> <dt>0x00010000</dt></span></span> </dl>  | <span data-ttu-id="b1722-117">Если этот флаг установлен, **сксслукупклргуид** выполняет поиск суррогата.</span><span class="sxs-lookup"><span data-stu-id="b1722-117">If this flag is set, **SxsLookupClrGuid** searches for a surrogate.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <span data-ttu-id="b1722-118"><dt>**SxS \_ УТОЧНЯющий запрос GUID поиска для \_ \_ \_ \_ \_ класса CLR**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="b1722-118"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="b1722-119">Если этот флаг установлен, **сксслукупклргуид** выполняет поиск класса.</span><span class="sxs-lookup"><span data-stu-id="b1722-119">If this flag is set, **SxsLookupClrGuid** searches for a class.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <span data-ttu-id="b1722-120"><dt>**SxS \_ Поиск \_ по \_ идентификатору GUID CLR \_ найти \_ любой**</dt> <dt>0x00030000</dt></span><span class="sxs-lookup"><span data-stu-id="b1722-120"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_ANY**</dt> <dt>0x00030000</dt></span></span> </dl>                    | <span data-ttu-id="b1722-121">Это сочетание флагов поиска **SxS в \_ \_ CLR \_ GUID \_ Find \_ суррогат** и SxS Lookup CLR " **\_ \_ \_ \_ Find \_ CLR \_** ". Если заданы оба параметра, **сксслукупклргуид** сначала ищет суррогат, и только если он не находит его, а затем выполняет поиск класса.</span><span class="sxs-lookup"><span data-stu-id="b1722-121">This is a combination of the **SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE** and **SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS** flags; if both are set, **SxsLookupClrGuid** searches for a surrogate first, and only if it does not find one, then searches for a class.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="b1722-122">*пклсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1722-122">*pClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1722-123">Указатель на идентификатор GUID, по которому будет производиться поиск сведений о взаимооперациях в контексте активации.</span><span class="sxs-lookup"><span data-stu-id="b1722-123">A pointer to the GUID about which to search the activation context for interoperation information.</span></span> <span data-ttu-id="b1722-124">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b1722-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1722-125">*хакткткс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b1722-125">*hActCtx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1722-126">Если в параметре *dwFlags* задано использование флага **\_ \_ \_ \_ \_ Акткткс в таблице GUID поиска SxS** , то *Хакткткс* должен содержать обработчик контекста активации, возвращаемый функцией [**креатеакткткс**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="b1722-126">If the **SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX** flag is set in the *dwFlags* parameter, then *hActCtx* must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="b1722-127">В противном случае *хакткткс* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b1722-127">Otherwise, *hActCtx* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b1722-128">*пваутпутбуффер* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="b1722-128">*pvOutputBuffer* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1722-129">Указатель на буфер, в который копируются возвращаемые сведения.</span><span class="sxs-lookup"><span data-stu-id="b1722-129">Pointer to the buffer into which return information is copied.</span></span> <span data-ttu-id="b1722-130">Этот параметр может иметь значение NULL только в том случае, если параметр *кбаутпутбуффер* имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b1722-130">This parameter may be NULL-valued only if the *cbOutputBuffer* parameter is zero-valued.</span></span> <span data-ttu-id="b1722-131">Данные, помещаемые в этот буфер при выходе (если таковые имеются), состоят из структуры **\_ \_ \_ CLR со сведениями о GUID SxS** , за которыми следуют дополнительные строковые данные.</span><span class="sxs-lookup"><span data-stu-id="b1722-131">The data placed in this buffer on exit (if any) consists of a **SXS\_GUID\_INFORMATION\_CLR** structure followed by any additional string data required.</span></span> <span data-ttu-id="b1722-132">Дополнительные сведения см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="b1722-132">See the Remarks section below for more information.</span></span>

</dd> <dt>

<span data-ttu-id="b1722-133">*кбаутпутбуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1722-133">*cbOutputBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1722-134">Размер в байтах буфера, на который указывает параметр *пваутпутбуффер* .</span><span class="sxs-lookup"><span data-stu-id="b1722-134">Size in bytes of the buffer pointed to by the *pvOutputBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b1722-135">*пкбаутпутбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b1722-135">*pcbOutputBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1722-136">Указатель на переменную, в которой при выходе помещается размер возвращаемых данных (в байтах).</span><span class="sxs-lookup"><span data-stu-id="b1722-136">Pointer to a variable where the size, in bytes, of the return information is placed on exit.</span></span> <span data-ttu-id="b1722-137">Если параметр *кбаутпутбуффер* равен нулю или размер выходного буфера меньше, чем размер возвращаемых данных, то **сксслукупклргуид** завершается ошибкой, а [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, **\_ недостаточную для \_ буфера**.</span><span class="sxs-lookup"><span data-stu-id="b1722-137">If the *cbOutputBuffer* parameter is zero, or if the size of the output buffer is smaller than the size of the return information, then **SxsLookupClrGuid** fails and [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns an error of **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="b1722-138">В этом случае используйте значение в переменной, на которую указывает *пкбаутпутбуффер* , для выделения достаточного размера буфера, а затем вызовите **сксслукупклргуид** еще раз, чтобы получить нужную информацию.</span><span class="sxs-lookup"><span data-stu-id="b1722-138">In this case, use the value in the variable pointed to by *pcbOutputBuffer* to allocate a large enough buffer, and then call **SxsLookupClrGuid** again to retrieve the desired information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1722-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1722-139">Return value</span></span>

<span data-ttu-id="b1722-140">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b1722-140">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="b1722-141">Для получения дополнительных сведений об ошибке вызовите [ **GetLastError** .](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="b1722-141">For more error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>

## <a name="remarks"></a><span data-ttu-id="b1722-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1722-142">Remarks</span></span>

<span data-ttu-id="b1722-143">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b1722-143">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="b1722-144">Управляемые компоненты могут объявлять себя как поддерживающие управляемые "сборки взаимодействия", что позволяет неуправляемому потребителю компонента Win32 ссылаться на объявляемую сборку.</span><span class="sxs-lookup"><span data-stu-id="b1722-144">Managed components may declare themselves as supporting managed "interop assemblies" so as to allow an unmanaged Win32 component consumer to reference the declaring assembly.</span></span> <span data-ttu-id="b1722-145">Потребитель компонента может взаимодействовать с управляемым компонентом, вызывая [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="b1722-145">The component consumer can interact with the managed component by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on a GUID.</span></span> <span data-ttu-id="b1722-146">Уровень взаимодействия направляет запрос на создание объекта в платформа .NET Framework, создает экземпляр управляемого объекта и возвращает указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b1722-146">The interoperation layer routes the object creation request to .NET Framework, creates an instance of the managed object, and returns an interface pointer.</span></span>

<span data-ttu-id="b1722-147">**Сксслукупклргуид** позволяет платформам извлекать информацию, связанную с данным идентификатором GUID, в манифесте компонента, например имя его класса .NET, какая версия платформа .NET Framework требуется и какая сборка узла, в которой он находится.</span><span class="sxs-lookup"><span data-stu-id="b1722-147">**SxsLookupClrGuid** allows the frameworks to retrieve information associated with a given GUID in the component's manifest, such as what its .NET class name is, what version of the .NET Framework it requires, and what host assembly it is located in.</span></span> <span data-ttu-id="b1722-148">Управляемые компоненты публикуют сборку взаимодействия, содержащую несколько инструкций, связывающих идентификаторы GUID с именами сборок и типов, а среда выполнения .NET — построение экземпляров управляемых объектов при вызове [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="b1722-148">Managed components publish an interop assembly that contains a number of statements associating GUIDs with assembly and type names, and the .NET runtime brokers the construction of managed object instances when [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is called.</span></span>

<span data-ttu-id="b1722-149">Ниже приведен пример манифеста компонента, объявляющего GUID CLR и суррогат CLR, который **сксслукупклргуид** может искать:</span><span class="sxs-lookup"><span data-stu-id="b1722-149">The following is a sample component manifest declaring a CLR GUID and a CLR surrogate that **SxsLookupClrGuid** can look up:</span></span>

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

<span data-ttu-id="b1722-150">Поставщик взаимодействий вызовет **сксслукупклргуид** с указателем на GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" и получит в результате возврата имени класса "мисамплесуррогате", требуемой версии среды выполнения "1.0.3055" и текстового удостоверения "DotNet. Sample. суррогаты, Version =" 1.0.0.0 ", Type =" Interop "для компонента размещения.</span><span class="sxs-lookup"><span data-stu-id="b1722-150">An interoperation provider would call **SxsLookupClrGuid** with a pointer to the GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", and would receive in return the class name "MySampleSurrogate", the required runtime version "1.0.3055", and the textual identity "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" of the hosting component.</span></span>

<span data-ttu-id="b1722-151">Эти возвращаемые сведения должны содержаться и (или) ссылаться на структуру **\_ \_ \_ CLR со сведениями об идентификаторах SxS** , объявленной следующим образом.</span><span class="sxs-lookup"><span data-stu-id="b1722-151">This return information would be contained and/or referenced by a **SXS\_GUID\_INFORMATION\_CLR** structure declared as follows.</span></span>

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

<span data-ttu-id="b1722-152">Члены этой структуры содержат следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="b1722-152">The members of this structure contain the following information.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1722-153">Член</span><span class="sxs-lookup"><span data-stu-id="b1722-153">Member</span></span></th>
<th><span data-ttu-id="b1722-154">Описание</span><span class="sxs-lookup"><span data-stu-id="b1722-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b1722-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>кбсизе</strong></span><span class="sxs-lookup"><span data-stu-id="b1722-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span></span><br/></td>
<td><span data-ttu-id="b1722-156">Содержит размер структуры SXS_GUID_INFORMATION_CLR (это позволяет увеличить структуру в более поздних версиях).</span><span class="sxs-lookup"><span data-stu-id="b1722-156">Contains the size of the SXS_GUID_INFORMATION_CLR structure (this allows the structure to grow in later versions).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1722-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span><span class="sxs-lookup"><span data-stu-id="b1722-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span></span><br/></td>
<td><span data-ttu-id="b1722-158">Содержит одно из следующих двух значений флагов:</span><span class="sxs-lookup"><span data-stu-id="b1722-158">Contains one of the following two flag values:</span></span> <br/>
<ul>
<li><span data-ttu-id="b1722-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): указывает, что указанный GUID связан с &quot; суррогатом.&quot;</span><span class="sxs-lookup"><span data-stu-id="b1722-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): Indicates that the specified GUID was associated with a &quot;surrogate.&quot;</span></span></li>
<li><span data-ttu-id="b1722-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): указывает, что указанный GUID был связан с &quot; классом.&quot;</span><span class="sxs-lookup"><span data-stu-id="b1722-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): Indicates that the specified GUID was associated with a &quot;class.&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1722-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>пквсзрунтимеверсион</strong></span><span class="sxs-lookup"><span data-stu-id="b1722-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span></span><br/></td>
<td><span data-ttu-id="b1722-162">Указывает на строку расширенных символов, завершающуюся нулем, которая определяет версию среды выполнения, указанную в манифесте узла для этого класса.</span><span class="sxs-lookup"><span data-stu-id="b1722-162">Points to a zero-terminated wide-character string that identifies the version of the runtime specified in the host manifest for this class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1722-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>пквсзтипенаме</strong></span><span class="sxs-lookup"><span data-stu-id="b1722-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span></span><br/></td>
<td><span data-ttu-id="b1722-164">Указывает на строку расширенных символов, заканчивающуюся нулем, которая содержит имя класса .NET, связанного с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="b1722-164">Points to a zero-terminated wide-character string that contains the name of the .NET class associated with the specified GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1722-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>пквсзассемблидентити</strong></span><span class="sxs-lookup"><span data-stu-id="b1722-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span></span><br/></td>
<td><span data-ttu-id="b1722-166">Указывает на строку расширенных символов, завершающуюся нулем, которая содержит текстовое удостоверение сборки, в которой размещен этот класс.</span><span class="sxs-lookup"><span data-stu-id="b1722-166">Points to a zero-terminated wide-character string that contains the textual identity of the assembly that hosts this class.</span></span> <span data-ttu-id="b1722-167">Дополнительные сведения о текстовом удостоверении см. в разделе &quot; Указание полных имен типов &quot; в разделе &quot; обнаружение сведений о типах во время выполнения &quot; в разделе &quot; программирование с помощью платформа .NET Framework &quot; в пакете SDK для платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b1722-167">For more information about textual identity, see &quot;Specifying Fully Qualified Type Names&quot; under &quot;Discovering Type Information at Run Time&quot; under &quot;Programming with the .NET Framework&quot; in the .NET Framework SDK.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b1722-168">Неуправляемое приложение может использовать возвращенную информацию, чтобы загрузить правильную версию платформа .NET Framework, загрузить сборку, определенную элементом **пквсзассемблидентити** , а затем создать экземпляр класса с именем с помощью элемента **пквсзтипенаме** .</span><span class="sxs-lookup"><span data-stu-id="b1722-168">An unmanaged application can use the information returned in this fashion to load the right version of the .NET Framework, load the assembly identified by the **pcwszAssemblyIdentity** element, and then create an instance of the class named by the **pcwszTypeName** element.</span></span>

## <a name="examples"></a><span data-ttu-id="b1722-169">Примеры</span><span class="sxs-lookup"><span data-stu-id="b1722-169">Examples</span></span>

<span data-ttu-id="b1722-170">Используйте динамическую компоновку, как показано ниже, чтобы вызвать функцию **сксслукупклргуид** :</span><span class="sxs-lookup"><span data-stu-id="b1722-170">Use dynamic linking as follows to call the **SxsLookupClrGuid** function:</span></span>


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a><span data-ttu-id="b1722-171">Требования</span><span class="sxs-lookup"><span data-stu-id="b1722-171">Requirements</span></span>



| <span data-ttu-id="b1722-172">Требование</span><span class="sxs-lookup"><span data-stu-id="b1722-172">Requirement</span></span> | <span data-ttu-id="b1722-173">Значение</span><span class="sxs-lookup"><span data-stu-id="b1722-173">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1722-174">DLL</span><span class="sxs-lookup"><span data-stu-id="b1722-174">DLL</span></span><br/> | <dl> <span data-ttu-id="b1722-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1722-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1722-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1722-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1722-177">Изолированные приложения и параллельные сборки</span><span class="sxs-lookup"><span data-stu-id="b1722-177">Isolated Applications and Side-by-side Assemblies</span></span>](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[<span data-ttu-id="b1722-178">**креатеакткткс**</span><span class="sxs-lookup"><span data-stu-id="b1722-178">**CreateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[<span data-ttu-id="b1722-179">**активатеакткткс**</span><span class="sxs-lookup"><span data-stu-id="b1722-179">**ActivateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[<span data-ttu-id="b1722-180">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b1722-180">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
