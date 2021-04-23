---
title: атрибут user_marshal
description: '\_Атрибут ACF пользователя Marshal связывает именованный локальный тип на целевом языке (усерм-Type) с типом передачи (тип связи), который передается между клиентом и сервером.'
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal атрибута MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337025"
---
# <a name="user_marshal-attribute"></a><span data-ttu-id="039a9-104">Пользовательский \_ атрибут маршалирования</span><span class="sxs-lookup"><span data-stu-id="039a9-104">user\_marshal attribute</span></span>

<span data-ttu-id="039a9-105">Атрибут ACF **пользователя \_ Marshal** связывает именованный локальный тип на целевом языке (*усерм-Type*) с типом передачи (тип *связи*), который передается между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="039a9-105">The **user\_marshal** ACF attribute associates a named local type in the target language (*userm-type*) with a transfer type (*wire-type*) that is transferred between client and server.</span></span>

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="039a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="039a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="039a9-107">*усерм — тип*</span><span class="sxs-lookup"><span data-stu-id="039a9-107">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="039a9-108">Указывает идентификатор пользовательского типа данных для маршалирования.</span><span class="sxs-lookup"><span data-stu-id="039a9-108">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="039a9-109">Тип усерм не должен быть *поддерживающим* передачу и не должен быть типом, известным компилятору MIDL.</span><span class="sxs-lookup"><span data-stu-id="039a9-109">The *userm-type* need not be transmittable and need not be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="039a9-110">*Тип провода*</span><span class="sxs-lookup"><span data-stu-id="039a9-110">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="039a9-111">Указывает именованный тип данных передачи, который фактически передается между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="039a9-111">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="039a9-112">Тип сети должен быть базовым типом MIDL, предопределенным типом или идентификатором типа, который может быть передан по сети.</span><span class="sxs-lookup"><span data-stu-id="039a9-112">The wire type must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="039a9-113">*пфлагс*</span><span class="sxs-lookup"><span data-stu-id="039a9-113">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="039a9-114">Задает указатель на поле флага [**(**](unsigned.md) [**длинное**](long.md)целое).</span><span class="sxs-lookup"><span data-stu-id="039a9-114">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="039a9-115">Слово в высоком порядке определяет флаги представления данных NDR в соответствии с определением DCE для представления с плавающей запятой, с большим или прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="039a9-115">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="039a9-116">Слово нижнего порядка задает флаг контекста маршалирования.</span><span class="sxs-lookup"><span data-stu-id="039a9-116">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="039a9-117">Точный макет флагов описан в [ \_ функции Type усерсизе](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="039a9-117">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="039a9-118">*стартингсизе*</span><span class="sxs-lookup"><span data-stu-id="039a9-118">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="039a9-119">Задает текущий размер буфера (смещение) перед изменением размера объекта.</span><span class="sxs-lookup"><span data-stu-id="039a9-119">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="039a9-120">*Пусер \_ типеобжект*</span><span class="sxs-lookup"><span data-stu-id="039a9-120">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="039a9-121">Указывает указатель на объект *\_ типа усерм*.</span><span class="sxs-lookup"><span data-stu-id="039a9-121">Specifies a pointer to an object of *userm\_type*.</span></span>

</dd> <dt>

<span data-ttu-id="039a9-122">*Буфер*</span><span class="sxs-lookup"><span data-stu-id="039a9-122">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="039a9-123">Указывает текущий указатель буфера.</span><span class="sxs-lookup"><span data-stu-id="039a9-123">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="039a9-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="039a9-124">Remarks</span></span>

<span data-ttu-id="039a9-125">Каждый именованный локальный тип *усерм-Type* имеет корреспонденцию "один к одному" с *типом связи* "канал", который определяет прямое представление типа.</span><span class="sxs-lookup"><span data-stu-id="039a9-125">Each named local type, *userm-type*, has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="039a9-126">Необходимо предоставить подпрограммы для изменения размера данных для маршалирования, маршалирования и распаковки данных, а также для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="039a9-126">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="039a9-127">Дополнительные сведения об этих подоперациях см. [в описании \_ атрибута User Marshal](/windows/desktop/Rpc/the-user-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="039a9-127">For more information on these routines, see [The user\_marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute).</span></span> <span data-ttu-id="039a9-128">Обратите внимание, что при наличии в данных внедренных типов, которые также определены с помощью **\_ маршалирования пользователя** или \[ [**\[ проводного \_ маршалирования \]**](wire-marshal.md), необходимо также управлять обслуживанием этих внедренных типов.</span><span class="sxs-lookup"><span data-stu-id="039a9-128">Note that if there are embedded types in your data that are also defined with **user\_marshal** or \[ [**\[wire\_marshal\]**](wire-marshal.md), you need to manage the servicing of those embedded types also.</span></span>

<span data-ttu-id="039a9-129">*Тип провода* не может быть указателем интерфейса или полным указателем.</span><span class="sxs-lookup"><span data-stu-id="039a9-129">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="039a9-130">*Тип связи* должен иметь четко определенный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="039a9-130">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="039a9-131">Дополнительные сведения о том, как маршалировать данный *тип связи*, см. в разделе [правила упаковки для \_ \_ упаковки и](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) передачи данных.</span><span class="sxs-lookup"><span data-stu-id="039a9-131">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="039a9-132">*Усерм-Type* не должен быть указателем интерфейса, так как они могут быть упакованы напрямую.</span><span class="sxs-lookup"><span data-stu-id="039a9-132">The *userm-type* should not be an interface pointer as these can be marshaled directly.</span></span> <span data-ttu-id="039a9-133">Если тип пользователя является полным указателем, необходимо самостоятельно управлять псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="039a9-133">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

## <a name="examples"></a><span data-ttu-id="039a9-134">Примеры</span><span class="sxs-lookup"><span data-stu-id="039a9-134">Examples</span></span>

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a><span data-ttu-id="039a9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="039a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039a9-136">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="039a9-136">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="039a9-137">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="039a9-137">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="039a9-138">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="039a9-138">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="039a9-139">**представлять \_ как**</span><span class="sxs-lookup"><span data-stu-id="039a9-139">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="039a9-140">**без знака**</span><span class="sxs-lookup"><span data-stu-id="039a9-140">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="039a9-141">Атрибут пользовательской \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="039a9-141">The user\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="039a9-142">**проводное \_ маршалирование**</span><span class="sxs-lookup"><span data-stu-id="039a9-142">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="039a9-143">**ндржетусермаршалинфо**</span><span class="sxs-lookup"><span data-stu-id="039a9-143">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 