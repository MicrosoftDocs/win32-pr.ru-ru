---
title: атрибут ncacn_at_dsp
description: '\_ \_ Ключевое слово нкакн at DSP определяет AppleTalk DSP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987472"
---
# <a name="ncacn_at_dsp-attribute"></a><span data-ttu-id="124ac-105">\_атрибут нкакн в \_ DSP</span><span class="sxs-lookup"><span data-stu-id="124ac-105">ncacn\_at\_dsp attribute</span></span>

<span data-ttu-id="124ac-106">Ключевое слово **нкакн \_ at \_ DSP** определяет AppleTalk DSP в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="124ac-106">The **ncacn\_at\_dsp** keyword identifies AppleTalk DSP as the protocol family for the endpoint.</span></span> <span data-ttu-id="124ac-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="124ac-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="124ac-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="124ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="124ac-109">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="124ac-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="124ac-110">Задает символьную строку длиной до 22 байт.</span><span class="sxs-lookup"><span data-stu-id="124ac-110">Specifies a character string up to 22 bytes long.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="124ac-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="124ac-111">Remarks</span></span>

<span data-ttu-id="124ac-112">Синтаксис строки порта AppleTalk DSP, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="124ac-112">The syntax of the AppleTalk DSP port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="124ac-113">Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="124ac-113">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="124ac-114">Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="124ac-114">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="124ac-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="124ac-115">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="124ac-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="124ac-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="124ac-117">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="124ac-117">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="124ac-118">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="124ac-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="124ac-119">**Строковая привязка**</span><span class="sxs-lookup"><span data-stu-id="124ac-119">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 