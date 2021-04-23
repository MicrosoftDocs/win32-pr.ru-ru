---
title: Типы ловушек в нестандартные (SNMP. h)
description: Типы ловушек в спецификации "Стандартный" описывают предопределенный набор универсальных типов ловушек, которые отформатированы в соответствии со стандартом PDU ловушек стандарта.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892678"
---
# <a name="snmpv1-trap-types"></a><span data-ttu-id="b6269-103">Типы ловушек в нестандартные</span><span class="sxs-lookup"><span data-stu-id="b6269-103">SNMPv1 Trap Types</span></span>

<span data-ttu-id="b6269-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b6269-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b6269-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="b6269-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b6269-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="b6269-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b6269-107">Типы ловушек в спецификации "Стандартный" описывают предопределенный набор универсальных типов ловушек, которые отформатированы в соответствии со стандартом PDU ловушек стандарта.</span><span class="sxs-lookup"><span data-stu-id="b6269-107">The SNMPv1 trap types describe a predefined set of generic trap types that are formatted to comply with the SNMPv1 trap PDU standard.</span></span>



| <span data-ttu-id="b6269-108">Константа</span><span class="sxs-lookup"><span data-stu-id="b6269-108">Constant</span></span>                                                                                                                                                                                                          | <span data-ttu-id="b6269-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b6269-109">Description</span></span>                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <span data-ttu-id="b6269-110"><dt>**\_COLDSTART SNMP женериктрап \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6269-110"><dt>**SNMP\_GENERICTRAP\_COLDSTART**</dt></span></span> </dl>             | <span data-ttu-id="b6269-111">Указывает ловушку холодного запуска.</span><span class="sxs-lookup"><span data-stu-id="b6269-111">Indicates a cold start trap.</span></span> <span data-ttu-id="b6269-112">Агент инициализирует сущности протокола в управляемом режиме.</span><span class="sxs-lookup"><span data-stu-id="b6269-112">The agent is initializing protocol entities on the managed mode.</span></span> <span data-ttu-id="b6269-113">Он может изменять объекты в своем представлении.</span><span class="sxs-lookup"><span data-stu-id="b6269-113">It may alter objects in its view.</span></span><br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <span data-ttu-id="b6269-114"><dt>**\_WARMSTART SNMP женериктрап \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6269-114"><dt>**SNMP\_GENERICTRAP\_WARMSTART**</dt></span></span> </dl>             | <span data-ttu-id="b6269-115">Указывает на ловушку горячий запуск.</span><span class="sxs-lookup"><span data-stu-id="b6269-115">Indicates a warm start trap.</span></span> <span data-ttu-id="b6269-116">Выполняется повторная инициализация агента, но объекты в его представлении не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="b6269-116">The agent is reinitializing itself but it will not alter objects in its view.</span></span><br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <span data-ttu-id="b6269-117"><dt>**\_ЛИНКДОВН SNMP женериктрап \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6269-117"><dt>**SNMP\_GENERICTRAP\_LINKDOWN**</dt></span></span> </dl>                | <span data-ttu-id="b6269-118">Обозначает ловушку связи.</span><span class="sxs-lookup"><span data-stu-id="b6269-118">Indicates a link-down trap.</span></span> <span data-ttu-id="b6269-119">Состояние подключенного интерфейса изменилось на "отключено".</span><span class="sxs-lookup"><span data-stu-id="b6269-119">An attached interface has changed from the up state to the down state.</span></span> <span data-ttu-id="b6269-120">Первая переменная в списке привязок переменных определяет интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b6269-120">The first variable in the variable bindings list identifies the interface.</span></span><br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <span data-ttu-id="b6269-121"><dt>**\_ЛИНКУП SNMP женериктрап \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6269-121"><dt>**SNMP\_GENERICTRAP\_LINKUP**</dt></span></span> </dl>                      | <span data-ttu-id="b6269-122">Указывает ловушку связи.</span><span class="sxs-lookup"><span data-stu-id="b6269-122">Indicates a link-up trap.</span></span> <span data-ttu-id="b6269-123">Подключенный интерфейс изменился с начала до состояния up.</span><span class="sxs-lookup"><span data-stu-id="b6269-123">An attached interface has changed from the down start to the up state.</span></span> <span data-ttu-id="b6269-124">Первая переменная в списке привязок переменных определяет интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b6269-124">The first variable in the variable bindings list identifies the interface.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <span data-ttu-id="b6269-125"><dt>**\_АУСФАИЛУРЕ SNMP женериктрап \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6269-125"><dt>**SNMP\_GENERICTRAP\_AUTHFAILURE**</dt></span></span> </dl>       | <span data-ttu-id="b6269-126">Указывает ловушку сбоя проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b6269-126">Indicates an authentication failure trap.</span></span> <span data-ttu-id="b6269-127">Сущность SNMP отправила SNMP-сообщение, но оно неверно запросило отнести его к известному сообществу.</span><span class="sxs-lookup"><span data-stu-id="b6269-127">An SNMP entity has sent an SNMP message, but it has falsely claimed to belong to a known community.</span></span><br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <span data-ttu-id="b6269-128"><dt>**\_ЕГПНЕИГХЛОСС SNMP женериктрап \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6269-128"><dt>**SNMP\_GENERICTRAP\_EGPNEIGHLOSS**</dt></span></span> </dl>    | <span data-ttu-id="b6269-129">Указывает ловушку потери соседей ЕГП.</span><span class="sxs-lookup"><span data-stu-id="b6269-129">Indicates an EGP neighbor loss trap.</span></span> <span data-ttu-id="b6269-130">Одноранговый узел ЕГП изменился на состояние down.</span><span class="sxs-lookup"><span data-stu-id="b6269-130">An EGP peer has changed to the down state.</span></span> <span data-ttu-id="b6269-131">Первая переменная в списке привязок переменных определяет IP-адрес однорангового узла ЕГП.</span><span class="sxs-lookup"><span data-stu-id="b6269-131">The first variable in the variable bindings list identifies the IP address of the EGP peer.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <span data-ttu-id="b6269-132"><dt>**\_ЕНТЕРСПЕЦИФИК SNMP женериктрап \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6269-132"><dt>**SNMP\_GENERICTRAP\_ENTERSPECIFIC**</dt></span></span> </dl> | <span data-ttu-id="b6269-133">Указывает ловушку для конкретного предприятия.</span><span class="sxs-lookup"><span data-stu-id="b6269-133">Indicates an enterprise-specific trap.</span></span> <span data-ttu-id="b6269-134">Произошло непредвиденное событие.</span><span class="sxs-lookup"><span data-stu-id="b6269-134">An extraordinary event has occurred.</span></span> <span data-ttu-id="b6269-135">Он определяется в параметре *спеЦификтрап* с использованием значения, зависящего от Организации.</span><span class="sxs-lookup"><span data-stu-id="b6269-135">It is identified in the *specificTrap* parameter with an enterprise-specific value.</span></span><br/>               |



## <a name="requirements"></a><span data-ttu-id="b6269-136">Требования</span><span class="sxs-lookup"><span data-stu-id="b6269-136">Requirements</span></span>



| <span data-ttu-id="b6269-137">Требование</span><span class="sxs-lookup"><span data-stu-id="b6269-137">Requirement</span></span> | <span data-ttu-id="b6269-138">Значение</span><span class="sxs-lookup"><span data-stu-id="b6269-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b6269-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6269-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b6269-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6269-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="b6269-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6269-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b6269-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6269-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b6269-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6269-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6269-144"><dt>Протокол SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6269-144"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6269-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6269-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6269-146">Обзор протокола SNMP</span><span class="sxs-lookup"><span data-stu-id="b6269-146">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="b6269-147">Справочник по SNMP</span><span class="sxs-lookup"><span data-stu-id="b6269-147">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="b6269-148">Константы SNMP</span><span class="sxs-lookup"><span data-stu-id="b6269-148">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

