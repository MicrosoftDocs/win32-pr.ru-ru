---
description: Метод Жетобжекттекст \_ объекта свбемластеррор Возвращает текстовое представление объекта в формате MOF-файл (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: Метод SWbemLastError.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998667"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a><span data-ttu-id="13083-103">Свбемластеррор. Жетобжекттекст, \_ метод</span><span class="sxs-lookup"><span data-stu-id="13083-103">SWbemLastError.GetObjectText\_ method</span></span>

<span data-ttu-id="13083-104">Метод **жетобжекттекст \_** объекта [**свбемластеррор**](swbemlasterror.md) Возвращает текстовое представление объекта в формате [MOF-файл (MOF)](managed-object-format--mof-.md) .</span><span class="sxs-lookup"><span data-stu-id="13083-104">The **GetObjectText\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a textual rendering of the object in a [Managed Object Format (MOF)](managed-object-format--mof-.md) format.</span></span> <span data-ttu-id="13083-105">Этот MOF-объект можно использовать для вывода содержимого объекта.</span><span class="sxs-lookup"><span data-stu-id="13083-105">This MOF object can be used to display an object's contents.</span></span> <span data-ttu-id="13083-106">Обратите внимание, что возвращаемый MOF-текст не содержит всех сведений об объекте, но достаточно информации для компилятора MOF, чтобы иметь возможность повторно создать исходный объект.</span><span class="sxs-lookup"><span data-stu-id="13083-106">Notice that the MOF text that is returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="13083-107">Например, не будут найдены сведения о распространяемых квалификаторах или свойствах родительского класса.</span><span class="sxs-lookup"><span data-stu-id="13083-107">For instance, you will not find any information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="13083-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="13083-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13083-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13083-109">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="13083-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="13083-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13083-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="13083-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13083-112">Этот параметр зарезервирован и должен быть равен 0 (нулю), если он указан.</span><span class="sxs-lookup"><span data-stu-id="13083-112">This parameter is reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13083-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13083-113">Return value</span></span>

<span data-ttu-id="13083-114">В случае успеха этот метод возвращает строку, содержащую выходной текст.</span><span class="sxs-lookup"><span data-stu-id="13083-114">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13083-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="13083-115">Error codes</span></span>

<span data-ttu-id="13083-116">После завершения метода **жетобжекттекст \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="13083-116">Upon the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="13083-117">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="13083-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="13083-118">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="13083-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="13083-119">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="13083-119">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="13083-120">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="13083-120">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="13083-121">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="13083-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="13083-122">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="13083-122">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13083-123">Требования</span><span class="sxs-lookup"><span data-stu-id="13083-123">Requirements</span></span>



| <span data-ttu-id="13083-124">Требование</span><span class="sxs-lookup"><span data-stu-id="13083-124">Requirement</span></span> | <span data-ttu-id="13083-125">Значение</span><span class="sxs-lookup"><span data-stu-id="13083-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13083-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13083-126">Minimum supported client</span></span><br/> | <span data-ttu-id="13083-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13083-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13083-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13083-128">Minimum supported server</span></span><br/> | <span data-ttu-id="13083-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13083-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13083-130">Header</span><span class="sxs-lookup"><span data-stu-id="13083-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="13083-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13083-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="13083-132">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="13083-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="13083-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13083-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13083-134">DLL</span><span class="sxs-lookup"><span data-stu-id="13083-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13083-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13083-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="13083-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="13083-136">CLSID</span></span><br/>                    | <span data-ttu-id="13083-137">\_СВБЕМЛАСТЕРРОР CLSID</span><span class="sxs-lookup"><span data-stu-id="13083-137">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="13083-138">IID</span><span class="sxs-lookup"><span data-stu-id="13083-138">IID</span></span><br/>                      | <span data-ttu-id="13083-139">IID \_ исвбемластеррор</span><span class="sxs-lookup"><span data-stu-id="13083-139">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




