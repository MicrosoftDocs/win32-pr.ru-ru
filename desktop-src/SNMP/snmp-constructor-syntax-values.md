---
title: Значения синтаксиса конструктора SNMP (SNMP. h)
description: Значения синтаксиса конструктора SNMP описывают типы, совместимые с синтаксическим обозначением One (ASN. 1) стандарта кодирования.
ms.assetid: 8e3b6e00-51cf-4e39-a68e-dcf8fbe8ab3b
topic_type:
- apiref
api_name:
- ASN_SEQUENCE
- ASN_SEQUENCEOF
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484e58d7a92a3c75408db3160362d84e7891b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135655"
---
# <a name="snmp-constructor-syntax-values"></a><span data-ttu-id="f00f7-103">Значения синтаксиса конструктора SNMP</span><span class="sxs-lookup"><span data-stu-id="f00f7-103">SNMP Constructor Syntax Values</span></span>

<span data-ttu-id="f00f7-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f00f7-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f00f7-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f00f7-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f00f7-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="f00f7-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="f00f7-107">Значения синтаксиса конструктора SNMP описывают типы, совместимые с синтаксическим обозначением One (ASN. 1) стандарта кодирования.</span><span class="sxs-lookup"><span data-stu-id="f00f7-107">The SNMP Constructor Syntax Values describe types that are compliant with the Abstract Syntax Notation One (ASN.1) encoding standard.</span></span>



| <span data-ttu-id="f00f7-108">Константа</span><span class="sxs-lookup"><span data-stu-id="f00f7-108">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="f00f7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f00f7-109">Description</span></span>                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="ASN_SEQUENCE"></span><span id="asn_sequence"></span><dl> <span data-ttu-id="f00f7-110"><dt>**\_последовательность ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="f00f7-110"><dt>**ASN\_SEQUENCE**</dt></span></span> </dl>       | <span data-ttu-id="f00f7-111">Указывает, что сообщение является последовательностью ASN.</span><span class="sxs-lookup"><span data-stu-id="f00f7-111">Indicates that the message is an ASN sequence.</span></span><br/> |
| <span id="ASN_SEQUENCEOF"></span><span id="asn_sequenceof"></span><dl> <span data-ttu-id="f00f7-112"><dt>**ASN \_ секуенцеоф**</dt></span><span class="sxs-lookup"><span data-stu-id="f00f7-112"><dt>**ASN\_SEQUENCEOF**</dt></span></span> </dl> | <span data-ttu-id="f00f7-113">См \_ . последовательность ASN.</span><span class="sxs-lookup"><span data-stu-id="f00f7-113">See ASN\_SEQUENCE.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="f00f7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f00f7-114">Requirements</span></span>



| <span data-ttu-id="f00f7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f00f7-115">Requirement</span></span> | <span data-ttu-id="f00f7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f00f7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f00f7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f00f7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f00f7-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f00f7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="f00f7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f00f7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f00f7-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f00f7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f00f7-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f00f7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f00f7-122"><dt>Протокол SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="f00f7-122"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f00f7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f00f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f00f7-124">Обзор протокола SNMP</span><span class="sxs-lookup"><span data-stu-id="f00f7-124">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="f00f7-125">Справочник по SNMP</span><span class="sxs-lookup"><span data-stu-id="f00f7-125">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="f00f7-126">Константы SNMP</span><span class="sxs-lookup"><span data-stu-id="f00f7-126">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

