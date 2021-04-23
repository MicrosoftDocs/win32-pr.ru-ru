---
description: Свойство Locale объекта Свбемобжектпас содержит языковой стандарт пути к объекту.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Свойство Свбемобжектпас. locale (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693264"
---
# <a name="swbemobjectpathlocale-property"></a><span data-ttu-id="5f5a6-103">Свбемобжектпас. locale, свойство</span><span class="sxs-lookup"><span data-stu-id="5f5a6-103">SWbemObjectPath.Locale property</span></span>

<span data-ttu-id="5f5a6-104">Свойство **locale** объекта [**свбемобжектпас**](swbemobjectpath.md) содержит языковой стандарт пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="5f5a6-104">The **Locale** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the locale of object path.</span></span>

<span data-ttu-id="5f5a6-105">Если свойство **свбемобжектпас. locale** является частью автономного объекта [**свбемобжектпас**](swbemobjectpath.md) , оно доступно для чтения и записи и может использоваться для установки компонента языкового стандарта моникера.</span><span class="sxs-lookup"><span data-stu-id="5f5a6-105">When the **SWbemObjectPath.Locale** property is part of a standalone [**SWbemObjectPath**](swbemobjectpath.md) object, it is read/write and can be used to set the locale component of the moniker.</span></span>

<span data-ttu-id="5f5a6-106">Если доступ к свойству **свбемобжектпас. locale** осуществляется как часть свойства [**SWbemObject. Path \_**](swbemobject-path-.md) , он доступен только для чтения и сообщает значение локали, используемое в привязке к пространству имен, из которого был получен объект.</span><span class="sxs-lookup"><span data-stu-id="5f5a6-106">When the **SWbemObjectPath.Locale** property is accessed as part of a [**SWbemObject.Path\_**](swbemobject-path-.md) property, it is read-only and reports the value of the locale used in binding to the namespace from which the object was obtained.</span></span>

<span data-ttu-id="5f5a6-107">Для идентификаторов языковых стандартов Майкрософт формат строки — MS \_ XXXX, где XXXX — строка в шестнадцатеричном формате, указывающая код языка.</span><span class="sxs-lookup"><span data-stu-id="5f5a6-107">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="5f5a6-108">Например, идентификатором английского языка (США) является "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="5f5a6-108">For example, the American English locale identifier is "MS\_409".</span></span>

<span data-ttu-id="5f5a6-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5f5a6-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5f5a6-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5f5a6-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f5a6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f5a6-111">Syntax</span></span>


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a><span data-ttu-id="5f5a6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5f5a6-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="5f5a6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5f5a6-113">Requirements</span></span>



| <span data-ttu-id="5f5a6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5f5a6-114">Requirement</span></span> | <span data-ttu-id="5f5a6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5f5a6-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5a6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f5a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5a6-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f5a6-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f5a6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f5a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5a6-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f5a6-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f5a6-120">Header</span><span class="sxs-lookup"><span data-stu-id="5f5a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f5a6-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f5a6-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f5a6-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5f5a6-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f5a6-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f5a6-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f5a6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5f5a6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f5a6-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f5a6-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5f5a6-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="5f5a6-126">CLSID</span></span><br/>                    | <span data-ttu-id="5f5a6-127">\_СВБЕМОБЖЕКТПАС CLSID</span><span class="sxs-lookup"><span data-stu-id="5f5a6-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="5f5a6-128">IID</span><span class="sxs-lookup"><span data-stu-id="5f5a6-128">IID</span></span><br/>                      | <span data-ttu-id="5f5a6-129">IID \_ исвбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="5f5a6-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




