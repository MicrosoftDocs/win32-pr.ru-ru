---
title: v1_enum - атрибут
description: Атрибут \ v1 \_ enum \ указывает, что указанный перечисляемый тип передается как 32-разрядная сущность, а не как 16-разрядное значение по умолчанию.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum атрибута MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889675"
---
# <a name="v1_enum-attribute"></a><span data-ttu-id="0ffc6-104">\_атрибут перечисления v1</span><span class="sxs-lookup"><span data-stu-id="0ffc6-104">v1\_enum attribute</span></span>

<span data-ttu-id="0ffc6-105">Атрибут **\[ \_ перечисления \] v1** указывает, что указанный перечисляемый тип передается как 32-разрядная сущность, а не как 16-разрядное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ffc6-105">The **\[v1\_enum\]** attribute directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="0ffc6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ffc6-106">Parameters</span></span>

<span data-ttu-id="0ffc6-107">Этот атрибут не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ffc6-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ffc6-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ffc6-108">Remarks</span></span>

<span data-ttu-id="0ffc6-109">Использование атрибута **\[ \_ Enum \] версии v1** для передачи перечислимого типа в качестве 32-разрядной сущности повышает эффективность упаковки и распаковки данных, когда такое перечисление внедряется в структуры или объединения.</span><span class="sxs-lookup"><span data-stu-id="0ffc6-109">Using the **\[v1\_enum\]** attribute to transmit an enumerated type as a 32-bit entity increases the efficiency of marshaling and unmarshaling data when such an enumeration is embedded in structures or unions.</span></span>

<span data-ttu-id="0ffc6-110">Для повышения производительности мы рекомендуем применить атрибут **\[ \_ Enum \] версии v1** к перечислителям в 32-разрядных приложениях.</span><span class="sxs-lookup"><span data-stu-id="0ffc6-110">For improved performance, we recommend applying the **\[v1\_enum\]** attribute to enumerators in 32-bit applications.</span></span> <span data-ttu-id="0ffc6-111">Однако помните, что на 16-разрядных платформах компилятор C обрабатывает перечислимый тип как 16-разрядное [**целое**](int.md)число. Поэтому 16-разрядные клиентские приложения должны преобразовать типы [**enum**](enum.md) в [**Long**](long.md) для удаленной передачи, чтобы избежать перезаписи данных или отправки неверных значений.</span><span class="sxs-lookup"><span data-stu-id="0ffc6-111">Keep in mind, however, that on 16-bit platforms the C compiler treats an enumerated type as a 16-bit [**int**](int.md). Therefore 16-bit client applications need to convert [**enum**](enum.md) types to [**long**](long.md) for remote transmission in order to avoid overwriting data or sending incorrect values.</span></span>

## <a name="examples"></a><span data-ttu-id="0ffc6-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="0ffc6-112">Examples</span></span>

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a><span data-ttu-id="0ffc6-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ffc6-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ffc6-114">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="0ffc6-114">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="0ffc6-115">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="0ffc6-115">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0ffc6-116">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="0ffc6-116">**long**</span></span>](long.md)
</dt> </dl>

 

 




