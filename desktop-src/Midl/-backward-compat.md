---
title: backward_compat Switch
description: '\_Параметр совместимости/бакквард указывает компилятору MIDL отключить некоторые дополнительные функции при создании ЗАГЛУШЕК RPC/com.'
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672031"
---
# <a name="backward_compat-switch"></a><span data-ttu-id="52847-103">\_переключатель совместимости/бакквард</span><span class="sxs-lookup"><span data-stu-id="52847-103">/backward\_compat Switch</span></span>

<span data-ttu-id="52847-104">\_Параметр совместимости/бакквард указывает компилятору MIDL отключить некоторые дополнительные функции при создании ЗАГЛУШЕК RPC/com.</span><span class="sxs-lookup"><span data-stu-id="52847-104">The /backward\_compat switch directs the MIDL compiler to turn off some advanced features when generating RPC/COM stubs.</span></span>

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a><span data-ttu-id="52847-105">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="52847-105">Switch Options</span></span>

<span data-ttu-id="52847-106">*\_Размер майбенулл*</span><span class="sxs-lookup"><span data-stu-id="52847-106">*maybenull\_sizeis*</span></span><dl> <span data-ttu-id="52847-107">Применяет атрибут [ \[ отключения \_ \_ проверки \] согласованности](disable-consistence-check.md) ко всей компиляции MIDL.</span><span class="sxs-lookup"><span data-stu-id="52847-107">Applies the [\[disable\_consistency\_check\]](disable-consistence-check.md) attribute to an entire MIDL compilation.</span></span>  
</dl>

<span data-ttu-id="52847-108">*нулевое \_ алигнментгап*</span><span class="sxs-lookup"><span data-stu-id="52847-108">*zeroout\_alignmentgap*</span></span><dl> <span data-ttu-id="52847-109">Отключает нулевые промежутки в упакованном буфере.</span><span class="sxs-lookup"><span data-stu-id="52847-109">Turns off zeroing out gaps in the marshaled buffer.</span></span>  
</dl>

<span data-ttu-id="52847-110">*\_Преобразование BSTR бивалуе \_*</span><span class="sxs-lookup"><span data-stu-id="52847-110">*BSTR\_byvalue\_escaping*</span></span><dl> <span data-ttu-id="52847-111">Направляет компилятор MIDL для обработки escape-последовательностей, таких как € ̃ \\ нâ €™ или ̃ \\ тâ™ € в bstrs.</span><span class="sxs-lookup"><span data-stu-id="52847-111">Directs the MIDL compiler to honor escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in BSTRs.</span></span>  
</dl>

<span data-ttu-id="52847-112">*значение \_ DefaultValue для строки*</span><span class="sxs-lookup"><span data-stu-id="52847-112">*string\_defaultvalue*</span></span><dl> <span data-ttu-id="52847-113">Заставляет компилятор MIDL применяет строки в атрибутах [**\[ DefaultValue \]**](defaultvalue.md) к типу VARIANT. VT \_ I4 Type перед приведением значения к правильному типу.</span><span class="sxs-lookup"><span data-stu-id="52847-113">Forces the MIDL compiler to coerce strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span>  
</dl>

<span data-ttu-id="52847-114">*со знаком \_ WCHAR \_ t*</span><span class="sxs-lookup"><span data-stu-id="52847-114">*signed\_wchar\_t*</span></span><dl> <span data-ttu-id="52847-115">Направляет MIDL для интерпретации типа WCHAR \_ t как подписанного на совместимость с Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="52847-115">Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>  
</dl>

## <a name="remarks"></a><span data-ttu-id="52847-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52847-116">Remarks</span></span>

-   <span data-ttu-id="52847-117">*\_ Размер майбенулл*: см \[ . раздел \_ отключение \_ проверки согласованности \] .</span><span class="sxs-lookup"><span data-stu-id="52847-117">*maybenull\_sizeis*: See \[disable\_consistency\_check\].</span></span>
-   <span data-ttu-id="52847-118">*нулевое \_ алигнментгап*: когда IDL компилируются с параметром "Target NT60 или выше", MIDL создаст заглушки, которые обнуляют любые пробелы выравнивания между элементами или структурой в сетевом буфере.</span><span class="sxs-lookup"><span data-stu-id="52847-118">*zeroout\_alignmentgap*: When IDLs are compiled with â€“target NT60 or higher, MIDL will create stubs that zero out any alignment gaps between members or a structure in the wire buffer.</span></span> <span data-ttu-id="52847-119">Параметр командной строки/бакквард с функцией *\_ совместимости нулевого значения \_ алигнментгап* направляет MIDL для отключения этой функции.</span><span class="sxs-lookup"><span data-stu-id="52847-119">The command line switch */backward\_compat zeroout\_alignmentgap* directs MIDL to disable this feature.</span></span>

    <span data-ttu-id="52847-120">В следующем примере структуры проводной буфер содержит 7-байтный разрыв выравнивания для выравнивания элемента Hyper до 8 после элемента char.</span><span class="sxs-lookup"><span data-stu-id="52847-120">In the following example structure, the wire buffer contains a 7 byte alignment gap to align the hyper member to 8 after the char member.</span></span> <span data-ttu-id="52847-121">При использовании параметра target NT60 или более поздней версии MIDL отменяет этот разрыв, пока не будет использован параметр.</span><span class="sxs-lookup"><span data-stu-id="52847-121">With â€“target NT60 or higher, MIDL will zero out that gap unless the switch is used.</span></span>

    <span data-ttu-id="52847-122">IDL-файл:</span><span class="sxs-lookup"><span data-stu-id="52847-122">IDL file:</span></span>

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    <span data-ttu-id="52847-123">Этот параметр обеспечивает небольшое повышение производительности с потенциально значительным увеличением риска раскрытия.</span><span class="sxs-lookup"><span data-stu-id="52847-123">This switch can provide a slight performance improvement with potentially significant increases in disclosure risk.</span></span>

-   <span data-ttu-id="52847-124">*\_ Escape- \_ Преобразование бивалуе*~. по умолчанию компилятор MIDL не обрабатывает escape-последовательности, такие как € ̃ \\ нâ €™ или тâ, \\ то есть™ в строковых константах для OLE-автоматизации при преобразовании строковой константы в типы VT \_ LPSTR или VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="52847-124">*BSTR\_byvalue\_escaping*: By default, the MIDL compiler does not process escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in string constants for OLE Automation when converting a string constant to types VT\_LPSTR or VT\_LPWSTR.</span></span> <span data-ttu-id="52847-125">При этом параметре обратной совместимости вычисляются escape-последовательности.</span><span class="sxs-lookup"><span data-stu-id="52847-125">With this backward compatibility switch option, the escape sequences are evaluated.</span></span>
-   <span data-ttu-id="52847-126">*\_ DefaultValue = строка*: заставляет компилятор MIDL применять числовые строки в атрибутах [**\[ \] DefaultValue**](defaultvalue.md) к Variant. VT \_ I4 Type перед приведением значения к правильному типу.</span><span class="sxs-lookup"><span data-stu-id="52847-126">*string\_defaultvalue*: Forces the MIDL compiler to coerce numeric strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span> <span data-ttu-id="52847-127">В некоторых случаях это может привести к утрате точности, поэтому этот параметр не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="52847-127">This can lead to loss of precision in some cases, so this switch option is not recommended.</span></span>
-   <span data-ttu-id="52847-128">*со знаком \_ WCHAR \_ t*: указывает MIDL обрабатывать \_ тип WCHAR t как подписанный для совместимости с Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="52847-128">*signed\_wchar\_t*: Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>

 

 




