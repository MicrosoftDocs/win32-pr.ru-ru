---
title: requestedit - атрибут
description: Атрибут \ рекуестедит \ указывает, что свойство поддерживает уведомление уведомление OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- атрибут рекуестедит MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650328"
---
# <a name="requestedit-attribute"></a><span data-ttu-id="2ca24-104">requestedit - атрибут</span><span class="sxs-lookup"><span data-stu-id="2ca24-104">requestedit attribute</span></span>

<span data-ttu-id="2ca24-105">Атрибут **\[ рекуестедит \]** указывает, что свойство поддерживает уведомление **уведомление OnRequestEdit** .</span><span class="sxs-lookup"><span data-stu-id="2ca24-105">The **\[requestedit\]** attribute indicates that the property supports the **OnRequestEdit** notification.</span></span>

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a><span data-ttu-id="2ca24-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ca24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca24-107">*необязательные атрибуты*</span><span class="sxs-lookup"><span data-stu-id="2ca24-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="2ca24-108">Ноль или несколько атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="2ca24-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="2ca24-109">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="2ca24-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2ca24-110">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="2ca24-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="2ca24-111">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="2ca24-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2ca24-112">Указывает имя функции в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="2ca24-112">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="2ca24-113">*params*</span><span class="sxs-lookup"><span data-stu-id="2ca24-113">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="2ca24-114">Ноль или более параметров функции.</span><span class="sxs-lookup"><span data-stu-id="2ca24-114">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ca24-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ca24-115">Remarks</span></span>

<span data-ttu-id="2ca24-116">Поддержка **уведомление OnRequestEdit** уведомления означает, что перед внесением изменений объект отправляет клиенту запрос на изменение свойства.</span><span class="sxs-lookup"><span data-stu-id="2ca24-116">Supporting **OnRequestEdit** notification means that, before a change is made, the object will send the client a request for permission to change a property.</span></span> <span data-ttu-id="2ca24-117">Объект может поддерживать привязку данных, но не имеет этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="2ca24-117">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="2ca24-118">Флаги</span><span class="sxs-lookup"><span data-stu-id="2ca24-118">Flags</span></span>

<span data-ttu-id="2ca24-119">ФУНКФЛАГ \_ фрекуестедит, варфлаг \_ фрекуестедит</span><span class="sxs-lookup"><span data-stu-id="2ca24-119">FUNCFLAG\_FREQUESTEDIT, VARFLAG\_FREQUESTEDIT</span></span>

## <a name="examples"></a><span data-ttu-id="2ca24-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="2ca24-120">Examples</span></span>

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a><span data-ttu-id="2ca24-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ca24-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca24-122">типефлагс</span><span class="sxs-lookup"><span data-stu-id="2ca24-122">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="2ca24-123">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="2ca24-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="2ca24-124">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="2ca24-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="2ca24-125">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="2ca24-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 