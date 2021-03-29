---
description: Метод Жетобжекттекст \_ объекта SWbemObject Возвращает текстовое представление объекта.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: Метод SWbemObject.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2447d8361d02626e1f5ea8fae1928ffd563d52ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647255"
---
# <a name="swbemobjectgetobjecttext_-method"></a><span data-ttu-id="9f26c-103">SWbemObject. Жетобжекттекст, \_ метод</span><span class="sxs-lookup"><span data-stu-id="9f26c-103">SWbemObject.GetObjectText\_ method</span></span>

<span data-ttu-id="9f26c-104">Метод **жетобжекттекст \_** объекта [**SWbemObject**](swbemobject.md) Возвращает текстовое представление объекта.</span><span class="sxs-lookup"><span data-stu-id="9f26c-104">The **GetObjectText\_** method of the [**SWbemObject**](swbemobject.md) object returns a textual rendering of the object.</span></span> <span data-ttu-id="9f26c-105">Этот объект можно использовать для вывода содержимого объекта.</span><span class="sxs-lookup"><span data-stu-id="9f26c-105">This object can be used to display an object's contents.</span></span> <span data-ttu-id="9f26c-106">В настоящее время в качестве выходного формата поддерживается только синтаксис MOF.</span><span class="sxs-lookup"><span data-stu-id="9f26c-106">Currently, only the MOF syntax is supported as an output format.</span></span> <span data-ttu-id="9f26c-107">Обратите внимание, что возвращенный текст MOF не содержит все сведения об объекте; MOF-текст содержит достаточно информации, чтобы компилятор MOF мог создать исходный объект заново.</span><span class="sxs-lookup"><span data-stu-id="9f26c-107">Notice that the MOF text returned does not contain all the information about the object; the MOF text contains only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="9f26c-108">Например, отсутствуют сведения о распространяемых квалификаторах или свойствах родительского класса.</span><span class="sxs-lookup"><span data-stu-id="9f26c-108">For instance, there is no information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="9f26c-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9f26c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f26c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f26c-110">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9f26c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f26c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f26c-112">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9f26c-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f26c-113">Зарезервировано и должно быть равно 0 (нулю), если оно указано.</span><span class="sxs-lookup"><span data-stu-id="9f26c-113">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f26c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f26c-114">Return value</span></span>

<span data-ttu-id="9f26c-115">В случае успеха этот метод возвращает строку, содержащую выходной текст.</span><span class="sxs-lookup"><span data-stu-id="9f26c-115">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9f26c-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9f26c-116">Error codes</span></span>

<span data-ttu-id="9f26c-117">После завершения метода **жетобжекттекст \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="9f26c-117">After the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9f26c-118">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9f26c-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9f26c-119">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="9f26c-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9f26c-120">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9f26c-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9f26c-121">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="9f26c-121">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="9f26c-122">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9f26c-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9f26c-123">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="9f26c-123">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9f26c-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="9f26c-124">Examples</span></span>

<span data-ttu-id="9f26c-125">Следующий код, взятый из [списка определения класса WMI в формате MOF в виде](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) кода VBScript в коллекции TechNet, извлекает и отображает текстовое представление определения класса WMI в синтаксисе MOF (MOF-файл).</span><span class="sxs-lookup"><span data-stu-id="9f26c-125">The following code, taken from the [List the Definition of a WMI Class in MOF Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript code sample in the TechNet Gallery, retrieves and displays the textual representation of a WMI class definition in MOF (Managed Object Format) syntax.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a><span data-ttu-id="9f26c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="9f26c-126">Requirements</span></span>



| <span data-ttu-id="9f26c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="9f26c-127">Requirement</span></span> | <span data-ttu-id="9f26c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="9f26c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f26c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f26c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9f26c-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f26c-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f26c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f26c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9f26c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f26c-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f26c-133">Header</span><span class="sxs-lookup"><span data-stu-id="9f26c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f26c-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f26c-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f26c-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9f26c-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="9f26c-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9f26c-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9f26c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9f26c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f26c-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f26c-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9f26c-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="9f26c-139">CLSID</span></span><br/>                    | <span data-ttu-id="9f26c-140">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="9f26c-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="9f26c-141">IID</span><span class="sxs-lookup"><span data-stu-id="9f26c-141">IID</span></span><br/>                      | <span data-ttu-id="9f26c-142">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="9f26c-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




