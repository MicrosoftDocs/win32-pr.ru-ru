---
title: wire_marshal - атрибут
description: Атрибут \ проводное \_ маршалирование \ задает тип данных, который будет использоваться для передачи (тип связи) вместо типа данных, зависящего от приложения (усерм-Type).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal атрибута MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104413988"
---
# <a name="wire_marshal-attribute"></a><span data-ttu-id="eeacf-104">атрибут проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="eeacf-104">wire\_marshal attribute</span></span>

<span data-ttu-id="eeacf-105">Атрибут **\[ проводного \_ маршалирования \]** задает тип данных, который будет использоваться для передачи ( *тип связи*) вместо типа данных, зависящего от приложения ( *усерм-Type*).</span><span class="sxs-lookup"><span data-stu-id="eeacf-105">The **\[wire\_marshal\]** attribute specifies a data type that will be used for transmission (the *wire-type*) instead of an application-specific data type (the *userm-type*).</span></span>

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="eeacf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eeacf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeacf-107">*Тип провода*</span><span class="sxs-lookup"><span data-stu-id="eeacf-107">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="eeacf-108">Указывает именованный тип данных передачи, который фактически передается между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="eeacf-108">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="eeacf-109">*Тип связи* должен быть базовым типом MIDL, предопределенным типом или идентификатором типа, который может быть передан по сети.</span><span class="sxs-lookup"><span data-stu-id="eeacf-109">The *wire-type* must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="eeacf-110">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="eeacf-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="eeacf-111">Тип, для которого *усерм-Type* станет псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="eeacf-111">The type for which *userm-type* will become an alias.</span></span>

</dd> <dt>

<span data-ttu-id="eeacf-112">*усерм — тип*</span><span class="sxs-lookup"><span data-stu-id="eeacf-112">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="eeacf-113">Указывает идентификатор пользовательского типа данных для маршалирования.</span><span class="sxs-lookup"><span data-stu-id="eeacf-113">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="eeacf-114">Это может быть любой тип, заданный *описателем типа*, при условии, что он имеет четко определенный размер.</span><span class="sxs-lookup"><span data-stu-id="eeacf-114">It can be any type, as given by the *type-specifier*, as long as it has a well-defined size.</span></span> <span data-ttu-id="eeacf-115">*Тип усерм* не может быть передающим, но должен быть типом, известным компилятору MIDL.</span><span class="sxs-lookup"><span data-stu-id="eeacf-115">The *userm-type* need not be transmittable but must be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="eeacf-116">*пфлагс*</span><span class="sxs-lookup"><span data-stu-id="eeacf-116">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="eeacf-117">Задает указатель на поле флага [**(**](unsigned.md) [**длинное**](long.md)целое).</span><span class="sxs-lookup"><span data-stu-id="eeacf-117">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="eeacf-118">Слово в высоком порядке определяет флаги представления данных NDR в соответствии с определением DCE для представления с плавающей запятой, с большим или прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="eeacf-118">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="eeacf-119">Слово нижнего порядка задает флаг контекста маршалирования.</span><span class="sxs-lookup"><span data-stu-id="eeacf-119">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="eeacf-120">Точный макет флагов описан в [ \_ функции Type усерсизе](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="eeacf-120">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="eeacf-121">*стартингсизе*</span><span class="sxs-lookup"><span data-stu-id="eeacf-121">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="eeacf-122">Задает текущий размер буфера (смещение) перед изменением размера объекта.</span><span class="sxs-lookup"><span data-stu-id="eeacf-122">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="eeacf-123">*Пусер \_ типеобжект*</span><span class="sxs-lookup"><span data-stu-id="eeacf-123">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="eeacf-124">Указывает указатель на объект *\_ типа усерм.*</span><span class="sxs-lookup"><span data-stu-id="eeacf-124">Specifies a pointer to an object of *userm\_type.*</span></span>

</dd> <dt>

<span data-ttu-id="eeacf-125">*Буфер*</span><span class="sxs-lookup"><span data-stu-id="eeacf-125">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="eeacf-126">Указывает текущий указатель буфера.</span><span class="sxs-lookup"><span data-stu-id="eeacf-126">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eeacf-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eeacf-127">Remarks</span></span>

<span data-ttu-id="eeacf-128">Каждый тип данных, относящийся к конкретному приложению, *усерм-Type,* имеет корреспонденцию "один к одному" с *типом связи* , который определяет сетевое представление типа.</span><span class="sxs-lookup"><span data-stu-id="eeacf-128">Each application-specific data type, *userm-type,* has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="eeacf-129">Необходимо предоставить подпрограммы для изменения размера данных для маршалирования, маршалирования и распаковки данных, а также для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="eeacf-129">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="eeacf-130">Обратите внимание, что при наличии в данных внедренных типов, которые также определены с помощью **\[ проводного \_ маршалирования \]** или **\[** [**пользовательского \_ маршалирования**](user-marshal.md) **\]** , необходимо также управлять обслуживанием этих внедренных типов.</span><span class="sxs-lookup"><span data-stu-id="eeacf-130">Note that if there are embedded types in your data that are also defined with **\[wire\_marshal\]** or **\[**[**user\_marshal**](user-marshal.md)**\]**, you need to manage the servicing of those embedded types also.</span></span> <span data-ttu-id="eeacf-131">Дополнительные сведения об этих подоперациях см. [в описании атрибута Wired \_ Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="eeacf-131">For more information on these routines, see [The wire\_marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute).</span></span>

<span data-ttu-id="eeacf-132">Реализация должна соответствовать правилам маршалинга в соответствии со спецификацией использование-DCE.</span><span class="sxs-lookup"><span data-stu-id="eeacf-132">Your implementation must follow the marshalling rules according to the OSF-DCE specification.</span></span> <span data-ttu-id="eeacf-133">Подробные сведения о синтаксисе перемещения NDR см. в статье [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) .</span><span class="sxs-lookup"><span data-stu-id="eeacf-133">Details about NDR transfer syntax can be found at [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).</span></span> <span data-ttu-id="eeacf-134">Не рекомендуется использовать передачу по **\[ сети \_ \]** , если вы не знакомы с протоколом передачи по сети.</span><span class="sxs-lookup"><span data-stu-id="eeacf-134">It is not recommended to use **\[wire\_marshal\]** if you are not familiar with the wire protocol.</span></span>

<span data-ttu-id="eeacf-135">*Тип провода* не может быть указателем интерфейса или полным указателем.</span><span class="sxs-lookup"><span data-stu-id="eeacf-135">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="eeacf-136">*Тип связи* должен иметь четко определенный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="eeacf-136">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="eeacf-137">Дополнительные сведения о том, как маршалировать данный *тип связи*, см. в разделе [правила упаковки для \_ \_ упаковки и](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) передачи данных.</span><span class="sxs-lookup"><span data-stu-id="eeacf-137">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="eeacf-138">*Усерм-Type* не должен быть указателем интерфейса, так как они могут быть упакованы напрямую.</span><span class="sxs-lookup"><span data-stu-id="eeacf-138">The *userm-type* should not be an interface pointer because these can be marshaled directly.</span></span> <span data-ttu-id="eeacf-139">Если тип пользователя является полным указателем, необходимо самостоятельно управлять псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="eeacf-139">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

<span data-ttu-id="eeacf-140">Нельзя использовать атрибут **\[ Wired \_ Marshal \]** с **\[** [](allocate.md) **\]** атрибутом allocate прямо или косвенно, так как модуль NDR не контролирует выделение памяти для переданного типа.</span><span class="sxs-lookup"><span data-stu-id="eeacf-140">You cannot use the **\[wire\_marshal\]** attribute with the **\[**[**allocate**](allocate.md)**\]** attribute, either directly or indirectly, because the NDR engine does not control memory allocation for the transmitted type.</span></span>

## <a name="examples"></a><span data-ttu-id="eeacf-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="eeacf-141">Examples</span></span>

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a><span data-ttu-id="eeacf-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eeacf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeacf-143">**allocate**</span><span class="sxs-lookup"><span data-stu-id="eeacf-143">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="eeacf-144">Представление данных</span><span class="sxs-lookup"><span data-stu-id="eeacf-144">Data Representation</span></span>](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[<span data-ttu-id="eeacf-145">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="eeacf-145">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="eeacf-146">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="eeacf-146">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="eeacf-147">**ндржетусермаршалинфо**</span><span class="sxs-lookup"><span data-stu-id="eeacf-147">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[<span data-ttu-id="eeacf-148">Атрибут Wired \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="eeacf-148">The wire\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="eeacf-149">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="eeacf-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="eeacf-150">**без знака**</span><span class="sxs-lookup"><span data-stu-id="eeacf-150">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="eeacf-151">**Пользовательская \_ Упаковка**</span><span class="sxs-lookup"><span data-stu-id="eeacf-151">**user\_marshal**</span></span>](user-marshal.md)
</dt> </dl>

 

 