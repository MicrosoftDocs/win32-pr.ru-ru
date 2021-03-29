---
title: usesgetlasterror - атрибут
description: Атрибут \ усесжетластеррор \ сообщает вызывающему объекту, что он может вызвать GetLastError для получения кода ошибки.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- атрибут усесжетластеррор MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790003"
---
# <a name="usesgetlasterror-attribute"></a><span data-ttu-id="d88a8-104">usesgetlasterror - атрибут</span><span class="sxs-lookup"><span data-stu-id="d88a8-104">usesgetlasterror attribute</span></span>

<span data-ttu-id="d88a8-105">Атрибут **\[ усесжетластеррор \]** сигнализирует вызывающему объекту, что он может вызвать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) для получения кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="d88a8-105">The **\[usesgetlasterror\]** attribute signals the caller that it can call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a><span data-ttu-id="d88a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d88a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88a8-107">*атрибуты модуля*</span><span class="sxs-lookup"><span data-stu-id="d88a8-107">*module-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a8-108">Ноль или несколько атрибутов MIDL, которые будут применены к [**модулю**](module.md).</span><span class="sxs-lookup"><span data-stu-id="d88a8-108">Zero or more MIDL attributes that will be applied to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="d88a8-109">*имя модуля*</span><span class="sxs-lookup"><span data-stu-id="d88a8-109">*module-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a8-110">Имя идентификатора [**модуля**](module.md).</span><span class="sxs-lookup"><span data-stu-id="d88a8-110">The identifier name of the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="d88a8-111">*Идентификатор записи*</span><span class="sxs-lookup"><span data-stu-id="d88a8-111">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a8-112">Указывает точку входа модуля — имя функции или целочисленный идентификационный номер.</span><span class="sxs-lookup"><span data-stu-id="d88a8-112">Specifies the module entry point–function name or integer-identification number.</span></span>

</dd> <dt>

<span data-ttu-id="d88a8-113">*другие атрибуты*</span><span class="sxs-lookup"><span data-stu-id="d88a8-113">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a8-114">Ноль или несколько атрибутов MIDL, которые будут применены к удаленной процедуре.</span><span class="sxs-lookup"><span data-stu-id="d88a8-114">Zero or more MIDL attributes that will be applied to the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="d88a8-115">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="d88a8-115">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a8-116">Тип данных, возвращаемых удаленной процедурой после завершения.</span><span class="sxs-lookup"><span data-stu-id="d88a8-116">The type of the data that the remote procedure will return upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="d88a8-117">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="d88a8-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a8-118">Имя удаленной процедуры, как определено в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="d88a8-118">The name of the remote procedure as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="d88a8-119">*Param-List*</span><span class="sxs-lookup"><span data-stu-id="d88a8-119">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d88a8-120">Ноль или более параметров для удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="d88a8-120">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d88a8-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d88a8-121">Remarks</span></span>

<span data-ttu-id="d88a8-122">Атрибут **\[ усесжетластеррор \]** можно задать в точке входа модуля, если эта точка входа использует функцию Windows [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) для возврата кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="d88a8-122">The **\[usesgetlasterror\]** attribute can be set on a module entry point, if that entry point uses the Windows function [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return error codes.</span></span> <span data-ttu-id="d88a8-123">Атрибут сообщает вызывающему объекту, что при возникновении ошибки при вызове этой функции вызывающий объект может вызвать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) для получения кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="d88a8-123">The attribute tells the caller that, if there is an error when calling that function, the caller can then call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

## <a name="examples"></a><span data-ttu-id="d88a8-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="d88a8-124">Examples</span></span>

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="d88a8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d88a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88a8-126">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="d88a8-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="d88a8-127">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="d88a8-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d88a8-128">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="d88a8-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 