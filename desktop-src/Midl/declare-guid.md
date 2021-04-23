---
title: Ключевое слово declare_guid
description: '\_Ключевое слово Declare GUID предписывает MIDL создавать переменную GUID в создаваемом файле заголовка.'
keywords:
- declare_guid ключевого слова MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105720015"
---
# <a name="declare_guid-keyword"></a><span data-ttu-id="bac35-104">\_ключевое слово Declare GUID</span><span class="sxs-lookup"><span data-stu-id="bac35-104">declare\_guid keyword</span></span>

<span data-ttu-id="bac35-105">Ключевое слово **Declare \_ GUID** предписывает MIDL создавать переменную GUID в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="bac35-105">The **declare\_guid** keyword instructs MIDL to emit a GUID variable into the generated header file.</span></span>

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a><span data-ttu-id="bac35-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bac35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bac35-107">*имя переменной*</span><span class="sxs-lookup"><span data-stu-id="bac35-107">*variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bac35-108">Задает имя переменной для идентификатора в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="bac35-108">Specifies a variable name for the identifier in the generated header file.</span></span>

</dd> <dt>

<span data-ttu-id="bac35-109">*guid*</span><span class="sxs-lookup"><span data-stu-id="bac35-109">*guid*</span></span>
</dt> <dd>

<span data-ttu-id="bac35-110">Указывает [идентификатор GUID](/windows/win32/api/guiddef/ns-guiddef-guid) , который будет применяться к имени переменной в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="bac35-110">Specifies the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) that will apply to the variable name in the generated header file.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bac35-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="bac35-111">Examples</span></span>

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a><span data-ttu-id="bac35-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bac35-112">Remarks</span></span>

<span data-ttu-id="bac35-113">Использование `declare_guid` эквивалентно использованию `cpp_quote` для создания вызова `EXTERN_GUID` макроса.</span><span class="sxs-lookup"><span data-stu-id="bac35-113">Using `declare_guid` is equivalent to using `cpp_quote` to generate an invocation of the `EXTERN_GUID` macro.</span></span>

<span data-ttu-id="bac35-114">Приведенный выше пример приводит к получению следующих выходных данных:</span><span class="sxs-lookup"><span data-stu-id="bac35-114">The above example results in the following output:</span></span>

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

<span data-ttu-id="bac35-115">`declare_guid`Инструкция предоставляется для удобства.</span><span class="sxs-lookup"><span data-stu-id="bac35-115">The `declare_guid` statement is provided as a convenience.</span></span> <span data-ttu-id="bac35-116">Преимущество этого метода в том, что он использует тот же синтаксис GUID, что и [ `uuid` атрибут](uuid.md).</span><span class="sxs-lookup"><span data-stu-id="bac35-116">It has the advantage of using the same GUID syntax as the [`uuid` attribute](uuid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bac35-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bac35-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac35-118">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="bac35-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="bac35-119">**cpp_quote**</span><span class="sxs-lookup"><span data-stu-id="bac35-119">**cpp_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="bac35-120">**uuid - атрибут**</span><span class="sxs-lookup"><span data-stu-id="bac35-120">**uuid attribute**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="bac35-121">**Структура GUID**</span><span class="sxs-lookup"><span data-stu-id="bac35-121">**GUID structure**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
