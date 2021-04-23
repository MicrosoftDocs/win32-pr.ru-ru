---
title: Типы запросов SNMP (SNMP. h)
description: Типы запросов SNMP используются для описания операции, которую служба SNMP запрашивает для выполнения агентом расширения.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492321"
---
# <a name="snmp-request-types"></a><span data-ttu-id="a626d-103">Типы запросов SNMP</span><span class="sxs-lookup"><span data-stu-id="a626d-103">SNMP Request Types</span></span>

<span data-ttu-id="a626d-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a626d-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a626d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="a626d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a626d-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="a626d-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="a626d-107">Типы запросов SNMP используются для описания операции, которую служба SNMP запрашивает для выполнения агентом расширения.</span><span class="sxs-lookup"><span data-stu-id="a626d-107">The SNMP Request Types are used to describe the operation that the SNMP service is requesting the extension agent to perform.</span></span>



| <span data-ttu-id="a626d-108">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="a626d-108">Constant/value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="a626d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a626d-109">Description</span></span>                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <span data-ttu-id="a626d-110"><dt>**Протокол SNMP \_ получение \_ расширения**</dt> <dt> \_ PDU SNMP \_ Get</dt></span><span class="sxs-lookup"><span data-stu-id="a626d-110"><dt>**SNMP\_EXTENSION\_GET**</dt> <dt>SNMP\_PDU\_GET</dt></span></span> </dl>                       | <span data-ttu-id="a626d-111">Получение значений указанных переменных.</span><span class="sxs-lookup"><span data-stu-id="a626d-111">Retrieve the value of values of the specified variables.</span></span><br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <span data-ttu-id="a626d-112"><dt>**Протокол SNMP \_ \_Get \_**</dt> -следующий <dt>SNMP- \_ \_ PDU</dt> расширения</span><span class="sxs-lookup"><span data-stu-id="a626d-112"><dt>**SNMP\_EXTENSION\_GET\_NEXT**</dt> <dt>SNMP\_PDU\_GETNEXT</dt></span></span> </dl>   | <span data-ttu-id="a626d-113">Получение значения или значений последователя лексикографическим порядком заданных переменных.</span><span class="sxs-lookup"><span data-stu-id="a626d-113">Retrieve the value or values of the lexicographic successor of the specified variables.</span></span><br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <span data-ttu-id="a626d-114"><dt>**Протокол SNMP \_ РАСШИРЕНИЕ \_ " \_ получить**</dt> многоблочный <dt> \_ \_ PDU SNMP</dt> "</span><span class="sxs-lookup"><span data-stu-id="a626d-114"><dt>**SNMP\_EXTENSION\_GET\_BULK**</dt> <dt>SNMP\_PDU\_GETBULK</dt></span></span> </dl>   | <span data-ttu-id="a626d-115">Поиск и получение нескольких значений с помощью одного запроса.</span><span class="sxs-lookup"><span data-stu-id="a626d-115">Search and retrieve multiple values with a single request.</span></span><br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <span data-ttu-id="a626d-116"><dt>**\_ \_ Проверка набора расширения \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="a626d-116"><dt>**SNMP\_EXTENSION\_SET\_TEST**</dt></span></span> </dl>                                                                           | <span data-ttu-id="a626d-117">Проверьте значения указанных переменных.</span><span class="sxs-lookup"><span data-stu-id="a626d-117">Validate the values of the specified variables.</span></span> <span data-ttu-id="a626d-118">Эта операция увеличивает вероятность успешной операции записи во время запроса на ФИКСАЦИю.</span><span class="sxs-lookup"><span data-stu-id="a626d-118">This operation maximizes the probability of a successful write operation during the COMMIT request.</span></span> <span data-ttu-id="a626d-119">Дополнительные сведения см. в описании функции [**снмпекстенсионкуерекс**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .</span><span class="sxs-lookup"><span data-stu-id="a626d-119">For more information, see the [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) function.</span></span><br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <span data-ttu-id="a626d-120"><dt>**Протокол SNMP \_ набор расширения " \_ \_ фиксация**</dt> <dt>SNMP- \_ \_ распределения</dt> "</span><span class="sxs-lookup"><span data-stu-id="a626d-120"><dt>**SNMP\_EXTENSION\_SET\_COMMIT**</dt> <dt>SNMP\_PDU\_SET</dt></span></span> </dl> | <span data-ttu-id="a626d-121">Запишите новые значения в указанные переменные.</span><span class="sxs-lookup"><span data-stu-id="a626d-121">Write the new values to the specified variables.</span></span><br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <span data-ttu-id="a626d-122"><dt>**\_расширение SNMP \_ Set \_ Undo**</dt></span><span class="sxs-lookup"><span data-stu-id="a626d-122"><dt>**SNMP\_EXTENSION\_SET\_UNDO**</dt></span></span> </dl>                                                                           | <span data-ttu-id="a626d-123">Сбросьте значения указанных переменных до запроса ФИКСАЦИи.</span><span class="sxs-lookup"><span data-stu-id="a626d-123">Reset the values of the specified variables to their values before the COMMIT request.</span></span><br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <span data-ttu-id="a626d-124"><dt>**\_ \_ Очистка набора расширений \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="a626d-124"><dt>**SNMP\_EXTENSION\_SET\_CLEANUP**</dt></span></span> </dl>                                                                  | <span data-ttu-id="a626d-125">Освободите ресурсы, выделенные в предыдущих запросах и операциях.</span><span class="sxs-lookup"><span data-stu-id="a626d-125">Release the resources allocated in previous requests and operations.</span></span><br/>                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="a626d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a626d-126">Requirements</span></span>



| <span data-ttu-id="a626d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a626d-127">Requirement</span></span> | <span data-ttu-id="a626d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a626d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a626d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a626d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a626d-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a626d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="a626d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a626d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a626d-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a626d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a626d-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a626d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a626d-134"><dt>Протокол SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a626d-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a626d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a626d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a626d-136">Обзор протокола SNMP</span><span class="sxs-lookup"><span data-stu-id="a626d-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="a626d-137">Справочник по SNMP</span><span class="sxs-lookup"><span data-stu-id="a626d-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="a626d-138">Константы SNMP</span><span class="sxs-lookup"><span data-stu-id="a626d-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

