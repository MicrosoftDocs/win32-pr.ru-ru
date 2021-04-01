---
description: Возвращает XML-представление объекта или экземпляра. Текстовый файл форматируется в формате XML, указанном, как показано в Вбемобжекттекстформатенум.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Метод SWbemObjectEx.GetText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081475"
---
# <a name="swbemobjectexgettext_-method"></a><span data-ttu-id="adf68-104">Свбемобжектекс. GetText, \_ метод</span><span class="sxs-lookup"><span data-stu-id="adf68-104">SWbemObjectEx.GetText\_ method</span></span>

<span data-ttu-id="adf68-105">Метод **gettext \_** объекта [**свбемобжектекс**](swbemobjectex.md) возвращает XML-представление объекта или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="adf68-105">The **GetText\_** method of the [**SWbemObjectEx**](swbemobjectex.md) object returns an XML representation of an object or instance.</span></span> <span data-ttu-id="adf68-106">Текстовый файл форматируется в формате XML, указанном, как показано в [**вбемобжекттекстформатенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span><span class="sxs-lookup"><span data-stu-id="adf68-106">The text file is formatted in the XML format specified as shown in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span></span>

<span data-ttu-id="adf68-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="adf68-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="adf68-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adf68-108">Syntax</span></span>


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="adf68-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="adf68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf68-110">*итекстформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="adf68-110">*iTextFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf68-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="adf68-111">Required.</span></span> <span data-ttu-id="adf68-112">Значение из [**вбемобжекттекстформатенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) , указывающее результирующий формат XML.</span><span class="sxs-lookup"><span data-stu-id="adf68-112">A value from [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) that specifies the resulting XML format.</span></span>

</dd> <dt>

<span data-ttu-id="adf68-113">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="adf68-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="adf68-114">Флаги зарезервированных операций.</span><span class="sxs-lookup"><span data-stu-id="adf68-114">Reserved operation flags.</span></span> <span data-ttu-id="adf68-115">Значение по умолчанию — 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="adf68-115">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="adf68-116">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="adf68-116">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="adf68-117">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который задает контекст для операции.</span><span class="sxs-lookup"><span data-stu-id="adf68-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span> <span data-ttu-id="adf68-118">Значение по умолчанию — NULL.</span><span class="sxs-lookup"><span data-stu-id="adf68-118">The default is null.</span></span> <span data-ttu-id="adf68-119">Дополнительные сведения о разрешенных парах "имя-значение" см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="adf68-119">For more information about the name/value pairs permitted, see Remarks below.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf68-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adf68-120">Return value</span></span>

<span data-ttu-id="adf68-121">Этот метод не имеет возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="adf68-121">This method has no return values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="adf68-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="adf68-122">Error codes</span></span>

<span data-ttu-id="adf68-123">После завершения метода **gettext \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="adf68-123">After completion of the **GetText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="adf68-124">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="adf68-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="adf68-125">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="adf68-125">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="adf68-126">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="adf68-126">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="adf68-127">Запрошенный формат не найден.</span><span class="sxs-lookup"><span data-stu-id="adf68-127">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="adf68-128">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="adf68-128">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="adf68-129">Один из параметров вызова указан неправильно.</span><span class="sxs-lookup"><span data-stu-id="adf68-129">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="adf68-130">**вбемерркритикалеррор** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="adf68-130">**wbemErrCriticalError** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="adf68-131">Произошла внутренняя, критическая, неожиданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="adf68-131">An internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="adf68-132">Отправьте отчет об этой ошибке в службу технической поддержки корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="adf68-132">Report this error to Microsoft Technical Support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adf68-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adf68-133">Remarks</span></span>

<span data-ttu-id="adf68-134">При создании [**свбемнамедвалуесет**](swbemnamedvalueset.md)допускаются только следующие пары "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="adf68-134">When constructing your [**SWbemNamedValueSet**](swbemnamedvalueset.md), only the following name/value pairs are permitted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adf68-135">Имя</span><span class="sxs-lookup"><span data-stu-id="adf68-135">Name</span></span></th>
<th><span data-ttu-id="adf68-136">Значение</span><span class="sxs-lookup"><span data-stu-id="adf68-136">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adf68-137">LocalOnly</span><span class="sxs-lookup"><span data-stu-id="adf68-137">LocalOnly</span></span></td>
<td><span data-ttu-id="adf68-138"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="adf68-138"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="adf68-139">Если <strong>значение — true</strong>, в результирующем XML-коде есть только локально определенные свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="adf68-139">If <strong>TRUE</strong>, only locally defined properties and methods are present in the resulting XML.</span></span> <span data-ttu-id="adf68-140">Значение по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="adf68-140">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf68-141">инклудекуалифиерс</span><span class="sxs-lookup"><span data-stu-id="adf68-141">IncludeQualifiers</span></span></td>
<td><span data-ttu-id="adf68-142"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="adf68-142"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="adf68-143">Если <strong>значение равно true</strong>, квалификаторы классов, экземпляров, свойств и методов включаются в результирующий XML.</span><span class="sxs-lookup"><span data-stu-id="adf68-143">If <strong>TRUE</strong>, qualifiers of classes, instances, properties, and methods are included in the resulting XML.</span></span> <span data-ttu-id="adf68-144">Значение по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="adf68-144">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf68-145">паслевел</span><span class="sxs-lookup"><span data-stu-id="adf68-145">PathLevel</span></span></td>
<td><span data-ttu-id="adf68-146"><strong>VT-I4</strong></span><span class="sxs-lookup"><span data-stu-id="adf68-146"><strong>VT-I4</strong></span></span><br/> <span data-ttu-id="adf68-147">Значение по умолчанию — 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="adf68-147">Default is 0 (zero).</span></span> <span data-ttu-id="adf68-148">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="adf68-148">Possible values are:</span></span><br/>
<ul>
<li><span data-ttu-id="adf68-149">0: <CLASS> элемент OR <INSTANCE> создается в зависимости от того, является ли объект классом или экземпляром.</span><span class="sxs-lookup"><span data-stu-id="adf68-149">0: A <CLASS> or <INSTANCE> element is created depending on whether the object is a class or instance.</span></span></li>
<li><span data-ttu-id="adf68-150">1: <VALUE.NAMEDOBJECT> создается элемент.</span><span class="sxs-lookup"><span data-stu-id="adf68-150">1: A <VALUE.NAMEDOBJECT> element is generated.</span></span></li>
<li><span data-ttu-id="adf68-151">2: <VALUE.OBJECTWITHLOCALPATH> создается элемент.</span><span class="sxs-lookup"><span data-stu-id="adf68-151">2: A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span></li>
<li><span data-ttu-id="adf68-152">3: <VALUE.OBJECTWITHPATH> создается элемент.</span><span class="sxs-lookup"><span data-stu-id="adf68-152">3: A <VALUE.OBJECTWITHPATH> element is generated.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf68-153">ексклудесистемпропертиес</span><span class="sxs-lookup"><span data-stu-id="adf68-153">ExcludeSystemProperties</span></span></td>
<td><span data-ttu-id="adf68-154"><strong>VT-BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="adf68-154"><strong>VT-BOOL</strong></span></span><br/> <span data-ttu-id="adf68-155">Если <strong>значение — true</strong>, системные свойства, такие как __NAMESPACE, исключаются из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="adf68-155">If <strong>TRUE</strong>, system properties, like __NAMESPACE, are excluded from the output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf68-156">инклудеклассоригин</span><span class="sxs-lookup"><span data-stu-id="adf68-156">IncludeClassOrigin</span></span></td>
<td><span data-ttu-id="adf68-157"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="adf68-157"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="adf68-158">Если <strong>значение — true</strong>, атрибут начала класса задается <PROPERTY> для <METHOD> элементов и.</span><span class="sxs-lookup"><span data-stu-id="adf68-158">If <strong>TRUE</strong>, the class origin attribute is set on the <PROPERTY> and <METHOD> elements.</span></span> <span data-ttu-id="adf68-159">Значение по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="adf68-159">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="adf68-160">Дополнительные сведения о создании [**свбемнамедвалуесет**](swbemnamedvalueset.md)см. в разделе [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md).</span><span class="sxs-lookup"><span data-stu-id="adf68-160">For more information about creating an [**SWbemNamedValueSet**](swbemnamedvalueset.md), see [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md).</span></span>

## <a name="examples"></a><span data-ttu-id="adf68-161">Примеры</span><span class="sxs-lookup"><span data-stu-id="adf68-161">Examples</span></span>

<span data-ttu-id="adf68-162">В следующем сценарии показано, как получить XML-представление определения класса [**\_ BIOS Win32**](/windows/desktop/CIMWin32Prov/win32-bios) .</span><span class="sxs-lookup"><span data-stu-id="adf68-162">The following script shows how to obtain an XML representation of the [**Win32\_Bios**](/windows/desktop/CIMWin32Prov/win32-bios) class definition.</span></span> <span data-ttu-id="adf68-163">Указав определенный экземпляр **Win32 \_ BIOS**, можно получить данные этого объекта в формате XML.</span><span class="sxs-lookup"><span data-stu-id="adf68-163">By specifying a particular instance of **Win32\_Bios**, you can obtain that object's data in XML.</span></span>


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a><span data-ttu-id="adf68-164">Требования</span><span class="sxs-lookup"><span data-stu-id="adf68-164">Requirements</span></span>



| <span data-ttu-id="adf68-165">Требование</span><span class="sxs-lookup"><span data-stu-id="adf68-165">Requirement</span></span> | <span data-ttu-id="adf68-166">Значение</span><span class="sxs-lookup"><span data-stu-id="adf68-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adf68-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adf68-167">Minimum supported client</span></span><br/> | <span data-ttu-id="adf68-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adf68-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="adf68-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adf68-169">Minimum supported server</span></span><br/> | <span data-ttu-id="adf68-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adf68-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="adf68-171">Header</span><span class="sxs-lookup"><span data-stu-id="adf68-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf68-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf68-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="adf68-173">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="adf68-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="adf68-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="adf68-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="adf68-175">DLL</span><span class="sxs-lookup"><span data-stu-id="adf68-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adf68-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf68-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="adf68-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="adf68-177">CLSID</span></span><br/>                    | <span data-ttu-id="adf68-178">\_СВБЕМОБЖЕКТЕКС CLSID</span><span class="sxs-lookup"><span data-stu-id="adf68-178">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="adf68-179">IID</span><span class="sxs-lookup"><span data-stu-id="adf68-179">IID</span></span><br/>                      | <span data-ttu-id="adf68-180">IID \_ исвбемобжектекс</span><span class="sxs-lookup"><span data-stu-id="adf68-180">IID\_ISWbemObjectEx</span></span><br/>                                                          |



 

