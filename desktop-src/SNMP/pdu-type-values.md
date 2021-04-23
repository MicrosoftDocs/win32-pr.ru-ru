---
title: Значения типа PDU (SNMP. h)
description: Значения типа PDU используются в поле типа PDU блока \_ распределения для описания его типа.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492324"
---
# <a name="pdu-type-values"></a><span data-ttu-id="55ab8-103">Значения типа PDU</span><span class="sxs-lookup"><span data-stu-id="55ab8-103">PDU Type Values</span></span>

<span data-ttu-id="55ab8-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="55ab8-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55ab8-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="55ab8-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="55ab8-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="55ab8-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="55ab8-107">Значения типа PDU используются в поле **\_ типа PDU** блока распределения для описания его типа.</span><span class="sxs-lookup"><span data-stu-id="55ab8-107">The PDU type values are used in the **pdu\_type** field of the PDU to describe its type.</span></span>



| <span data-ttu-id="55ab8-108">Константа</span><span class="sxs-lookup"><span data-stu-id="55ab8-108">Constant</span></span>                                                                                                                                                                   | <span data-ttu-id="55ab8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="55ab8-109">Description</span></span>                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <span data-ttu-id="55ab8-110"><dt>**\_Получение PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-110"><dt>**SNMP\_PDU\_GET**</dt></span></span> </dl>                | <span data-ttu-id="55ab8-111">Поиск и получение значения из указанной переменной SNMP.</span><span class="sxs-lookup"><span data-stu-id="55ab8-111">Search and retrieve a value from a specified SNMP variable.</span></span><br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <span data-ttu-id="55ab8-112"><dt>**SNMP- \_ PDU- \_ следующее**</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-112"><dt>**SNMP\_PDU\_GETNEXT**</dt></span></span> </dl>    | <span data-ttu-id="55ab8-113">Найдите и получите значение переменной SNMP, не зная точное имя переменной.</span><span class="sxs-lookup"><span data-stu-id="55ab8-113">Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.</span></span><br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <span data-ttu-id="55ab8-114"><dt>**отклик SNMP- \_ PDU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-114"><dt>**SNMP\_PDU\_RESPONSE**</dt></span></span> </dl> | <span data-ttu-id="55ab8-115">Ответьте на запрос на \_ Получение или прерывание SNMP-распределения SNMP \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="55ab8-115">Reply to an SNMP\_PDU\_GET or an SNMP\_PDU\_GETNEXT request.</span></span><br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <span data-ttu-id="55ab8-116"><dt>**\_набор PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-116"><dt>**SNMP\_PDU\_SET**</dt></span></span> </dl>                | <span data-ttu-id="55ab8-117">Сохранение значения в указанной переменной SNMP.</span><span class="sxs-lookup"><span data-stu-id="55ab8-117">Store a value in a specified SNMP variable.</span></span><br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <span data-ttu-id="55ab8-118"><dt>**\_V1TRAP PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-118"><dt>**SNMP\_PDU\_V1TRAP**</dt></span></span> </dl>       | <span data-ttu-id="55ab8-119">Указывает, что ловушка PDU форматируется для обеспечения соответствия стандарту стандарта стандартизации.</span><span class="sxs-lookup"><span data-stu-id="55ab8-119">Indicates that the PDU trap is formatted to conform with the SNMPv1 standard.</span></span><br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <span data-ttu-id="55ab8-120"><dt>**\_массив PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-120"><dt>**SNMP\_PDU\_GETBULK**</dt></span></span> </dl>    | <span data-ttu-id="55ab8-121">Поиск и получение нескольких значений с помощью одного запроса.</span><span class="sxs-lookup"><span data-stu-id="55ab8-121">Search and retrieve multiple values with a single request.</span></span><br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <span data-ttu-id="55ab8-122"><dt>**оповещения SNMP- \_ PDU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-122"><dt>**SNMP\_PDU\_INFORM**</dt></span></span> </dl>       | <span data-ttu-id="55ab8-123">Указывает PDU запроса уведомления.</span><span class="sxs-lookup"><span data-stu-id="55ab8-123">Indicates an inform request PDU.</span></span><br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <span data-ttu-id="55ab8-124"><dt>**\_ \_ ловушка PDU SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-124"><dt>**SNMP\_PDU\_TRAP**</dt></span></span> </dl>             | <span data-ttu-id="55ab8-125">Оповещает систему управления о непредвиденном событии в SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="55ab8-125">Alerts the management system to an extraordinary event under SNMPv2C.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="55ab8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="55ab8-126">Requirements</span></span>



| <span data-ttu-id="55ab8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="55ab8-127">Requirement</span></span> | <span data-ttu-id="55ab8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="55ab8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="55ab8-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55ab8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="55ab8-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55ab8-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="55ab8-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55ab8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="55ab8-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55ab8-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55ab8-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="55ab8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="55ab8-134"><dt>Протокол SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="55ab8-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55ab8-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55ab8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ab8-136">Обзор протокола SNMP</span><span class="sxs-lookup"><span data-stu-id="55ab8-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="55ab8-137">Справочник по SNMP</span><span class="sxs-lookup"><span data-stu-id="55ab8-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="55ab8-138">Константы SNMP</span><span class="sxs-lookup"><span data-stu-id="55ab8-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

