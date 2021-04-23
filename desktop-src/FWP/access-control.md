---
title: Управление доступом (платформа фильтрации Windows)
description: В платформе фильтрации Windows (WFP) служба базовой фильтрации (BFE) реализует стандартную модель управления доступом Windows, основанную на маркерах доступа и дескрипторах безопасности.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350985"
---
# <a name="access-control-windows-filtering-platform"></a><span data-ttu-id="826a8-103">Управление доступом (платформа фильтрации Windows)</span><span class="sxs-lookup"><span data-stu-id="826a8-103">Access Control (Windows Filtering Platform)</span></span>

<span data-ttu-id="826a8-104">В платформе фильтрации Windows (WFP) служба базовой фильтрации (BFE) реализует стандартную [модель управления доступом Windows](/windows/desktop/SecAuthZ/access-control-model) , основанную на маркерах доступа и дескрипторах безопасности.</span><span class="sxs-lookup"><span data-stu-id="826a8-104">In Windows Filtering Platform (WFP), the Base Filtering Engine (BFE) service implements the standard [Windows access control model](/windows/desktop/SecAuthZ/access-control-model) based on access tokens and security descriptors.</span></span>

## <a name="access-control-model"></a><span data-ttu-id="826a8-105">Модель контроля доступа</span><span class="sxs-lookup"><span data-stu-id="826a8-105">Access Control Model</span></span>

<span data-ttu-id="826a8-106">Дескрипторы безопасности могут быть заданы при добавлении новых объектов WFP, таких как фильтры и подслои.</span><span class="sxs-lookup"><span data-stu-id="826a8-106">Security descriptors can be specified when adding new WFP objects, such as filters and sub-layers.</span></span> <span data-ttu-id="826a8-107">Дескрипторы безопасности управляются с помощью функций управления WFP **фвпм \* GetSecurityInfo0** и **фвпм \* SetSecurityInfo0**, где \* *\** _ означает имя объекта WFP.</span><span class="sxs-lookup"><span data-stu-id="826a8-107">Security descriptors are managed using the WFP management functions **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0**, where \**\** _ stands for the WFP object's name.</span></span> <span data-ttu-id="826a8-108">Эти функции семантически идентичны функциям Windows [_ *жетсекуритинфо* \*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) и [**сетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="826a8-108">These functions are semantically identical to the Windows [_ *GetSecurityInfo*\*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

> [!Note]  
> <span data-ttu-id="826a8-109">Функции **фвпм \* SetSecurityInfo0** нельзя вызывать из явной транзакции.</span><span class="sxs-lookup"><span data-stu-id="826a8-109">The **Fwpm\*SetSecurityInfo0** functions cannot be called from within an explicit transaction.</span></span>

 

> [!Note]  
> <span data-ttu-id="826a8-110">Функции **фвпм \* SetSecurityInfo0** могут вызываться только из динамического сеанса, если они используются для управления динамическим объектом, созданным в рамках одного сеанса.</span><span class="sxs-lookup"><span data-stu-id="826a8-110">The **Fwpm\*SetSecurityInfo0** functions can only be called from within a dynamic session if they are being used to manage a dynamic object created within the same session.</span></span>

 

<span data-ttu-id="826a8-111">Дескриптор безопасности по умолчанию для обработчика фильтра (объект корневого обработчика на схеме ниже) выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="826a8-111">The default security descriptor for the filter engine (the root Engine object in the diagram below) is as follows.</span></span>

-   <span data-ttu-id="826a8-112">Предоставьте **Общий \_** доступ ко всем встроенным группам администраторов.</span><span class="sxs-lookup"><span data-stu-id="826a8-112">Grant **GENERIC\_ALL** (GA) access rights to the built-in Administrators group.</span></span>
-   <span data-ttu-id="826a8-113">Предоставьте права доступа универсального разрешения на **\_ Чтение** ( **GR) \_** универсального разрешения на **\_ выполнение** (GX) для операторов конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="826a8-113">Grant **GENERIC\_READ** (GR) **GENERIC\_WRITE** (GW) **GENERIC\_EXECUTE** (GX) access rights to network configuration operators.</span></span>
-   <span data-ttu-id="826a8-114">Предоставьте права доступа **гргвгкс** следующим идентификаторам безопасности службы (SSID): MPSSVC (брандмауэр Windows), Напажент (агент защиты доступа к сети), PolicyAgent (агент политики IPSec), RPCSS (удаленный вызов процедур) и Вдисервицехост (узел службы диагностики).</span><span class="sxs-lookup"><span data-stu-id="826a8-114">Grant **GRGWGX** access rights to the following service security identifiers (SSIDs): MpsSvc (Windows Firewall), NapAgent (Network Access Protection Agent), PolicyAgent (IPsec Policy Agent), RpcSs (Remote Procedure Call), and WdiServiceHost (Diagnostic Service Host).</span></span>
-   <span data-ttu-id="826a8-115">Предоставьте **фвпм \_ актрл \_ Open** и **фвпм \_ актрл \_ классифицировать** всем.</span><span class="sxs-lookup"><span data-stu-id="826a8-115">Grant **FWPM\_ACTRL\_OPEN** and **FWPM\_ACTRL\_CLASSIFY** to everyone.</span></span> <span data-ttu-id="826a8-116">(Это права доступа, характерные для WFP, описанные в таблице ниже.)</span><span class="sxs-lookup"><span data-stu-id="826a8-116">(These are WFP-specific access rights, described in table below.)</span></span>

<span data-ttu-id="826a8-117">Остальные дескрипторы безопасности по умолчанию являются производными через наследование.</span><span class="sxs-lookup"><span data-stu-id="826a8-117">The remaining default security descriptors are derived through inheritance.</span></span>

<span data-ttu-id="826a8-118">Существуют некоторые проверки доступа, например для **фвпм \* Add0**, **фвпм \* CreateEnumHandle0**, **фвпм \* SubscribeChanges0** вызовы функций, которые не могут быть выполнены на уровне отдельных объектов.</span><span class="sxs-lookup"><span data-stu-id="826a8-118">There are some access checks, such as for **Fwpm\*Add0**, **Fwpm\*CreateEnumHandle0**, **Fwpm\*SubscribeChanges0** function calls, that cannot be done at the individual object level.</span></span> <span data-ttu-id="826a8-119">Для этих функций существуют объекты контейнеров для каждого типа объектов.</span><span class="sxs-lookup"><span data-stu-id="826a8-119">For these functions, there are container objects for each object type.</span></span> <span data-ttu-id="826a8-120">Для стандартных типов объектов (например, поставщиков, выпусков, фильтров) существующие функции **фвпм \* GetSecurityInfo0** и **фвпм \* SetSecurityInfo0** перегружаются, что означает, что параметр **GUID** с нулевым значением определяет связанный контейнер.</span><span class="sxs-lookup"><span data-stu-id="826a8-120">For the standard object types (for example, providers, callouts, filters), the existing **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0** functions are overloaded, such that a null **GUID** parameter identifies the associated container.</span></span> <span data-ttu-id="826a8-121">Для других типов объектов (например, сетевых событий и сопоставлений безопасности IPsec) существуют явные функции для управления сведениями о безопасности контейнера.</span><span class="sxs-lookup"><span data-stu-id="826a8-121">For the other object types (for example, network events and IPsec security associations), there are explicit functions for managing the container's security information.</span></span>

<span data-ttu-id="826a8-122">BFE поддерживает автоматическое наследование записей контроля доступа (ACE) избирательного списка управления доступом (DACL).</span><span class="sxs-lookup"><span data-stu-id="826a8-122">BFE supports automatic inheritance of Discretionary Access Control List (DACL) access control entries (ACEs).</span></span> <span data-ttu-id="826a8-123">BFE не поддерживает элементы ACE системного списка управления доступом (SACL).</span><span class="sxs-lookup"><span data-stu-id="826a8-123">BFE does not support System Access Control List (SACL) ACEs.</span></span> <span data-ttu-id="826a8-124">Объекты наследуют ACE от своего контейнера.</span><span class="sxs-lookup"><span data-stu-id="826a8-124">Objects inherit ACEs from their container.</span></span> <span data-ttu-id="826a8-125">Контейнеры наследуют ACE от обработчика фильтров.</span><span class="sxs-lookup"><span data-stu-id="826a8-125">Containers inherit ACEs from the filter engine.</span></span> <span data-ttu-id="826a8-126">Пути распространения показаны на приведенной ниже схеме.</span><span class="sxs-lookup"><span data-stu-id="826a8-126">The propagation paths are shown in the diagram below.</span></span>

![Схема, на которой показаны пути распространения ACE, начиная с "Engine".](images/access-control.jpg)

<span data-ttu-id="826a8-128">Для стандартных типов объектов BFE применяет все универсальные и стандартные права доступа.</span><span class="sxs-lookup"><span data-stu-id="826a8-128">For the standard object types, BFE enforces all the generic and standard access rights.</span></span> <span data-ttu-id="826a8-129">Кроме того, WFP определяет следующие специальные права доступа.</span><span class="sxs-lookup"><span data-stu-id="826a8-129">In addition, WFP defines the following specific access rights.</span></span>



| <span data-ttu-id="826a8-130">Право доступа к WFP</span><span class="sxs-lookup"><span data-stu-id="826a8-130">WFP Access Right</span></span>                                                                                                                        | <span data-ttu-id="826a8-131">Описание</span><span class="sxs-lookup"><span data-stu-id="826a8-131">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="826a8-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**\_Добавление фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span><br/>                                       | <span data-ttu-id="826a8-133">Требуется для добавления объекта в контейнер.</span><span class="sxs-lookup"><span data-stu-id="826a8-133">Required to add an object to a container.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="826a8-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**ФВПМ \_ актрл \_ Добавить \_ ссылку**</span><span class="sxs-lookup"><span data-stu-id="826a8-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>                       | <span data-ttu-id="826a8-135">Требуется для создания связи с объектом.</span><span class="sxs-lookup"><span data-stu-id="826a8-135">Required to create an association to an object.</span></span> <span data-ttu-id="826a8-136">Например, чтобы добавить фильтр, который ссылается на выноску, вызывающий объект должен иметь \_ доступ к вызову Add Link.</span><span class="sxs-lookup"><span data-stu-id="826a8-136">For example, to add a filter that references a callout, the caller must have ADD\_LINK access to the callout.</span></span><br/> |
| <span data-ttu-id="826a8-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**ФВПМ \_ актрл \_ Начало \_ чтения \_ транзакция**</span><span class="sxs-lookup"><span data-stu-id="826a8-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span><br/>    | <span data-ttu-id="826a8-138">Требуется для начала явной транзакции чтения.</span><span class="sxs-lookup"><span data-stu-id="826a8-138">Required to begin an explicit read transaction.</span></span><br/>                                                                                                               |
| <span data-ttu-id="826a8-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**ФВПМ \_ актрл \_ начать \_ запись \_ транзакция**</span><span class="sxs-lookup"><span data-stu-id="826a8-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span><br/> | <span data-ttu-id="826a8-140">Требуется для начала явной транзакции записи.</span><span class="sxs-lookup"><span data-stu-id="826a8-140">Required to begin an explicit write transaction.</span></span><br/>                                                                                                              |
| <span data-ttu-id="826a8-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_классификация фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span><br/>                        | <span data-ttu-id="826a8-142">Требуется для классификации на уровне пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="826a8-142">Required to classify against a user-mode layer.</span></span><br/>                                                                                                               |
| <span data-ttu-id="826a8-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_перечисление АКТРЛ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span><br/>                                    | <span data-ttu-id="826a8-144">Требуется для перечисления объектов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="826a8-144">Required to enumerate the objects in a container.</span></span> <span data-ttu-id="826a8-145">Однако перечислитель возвращает только те объекты, к которым вызывающий объект \_ имеет \_ доступ фвпм актрл Read.</span><span class="sxs-lookup"><span data-stu-id="826a8-145">However, the enumerator only returns objects to which the caller has FWPM\_ACTRL\_READ access.</span></span><br/>              |
| <span data-ttu-id="826a8-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**ФВПМ \_ актрл \_ Open**</span><span class="sxs-lookup"><span data-stu-id="826a8-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span><br/>                                    | <span data-ttu-id="826a8-147">Требуется для открытия сеанса с BFE.</span><span class="sxs-lookup"><span data-stu-id="826a8-147">Required to open a session with BFE.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="826a8-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**\_Чтение фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span><br/>                                    | <span data-ttu-id="826a8-149">Требуется для чтения свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="826a8-149">Required to read an object's properties.</span></span><br/>                                                                                                                      |
| <span data-ttu-id="826a8-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_ \_ Статистика чтения фвпм \_ актрл**</span><span class="sxs-lookup"><span data-stu-id="826a8-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span><br/>                 | <span data-ttu-id="826a8-151">Требуется для чтения статистики.</span><span class="sxs-lookup"><span data-stu-id="826a8-151">Required to read statistics.</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="826a8-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**\_Подписка фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span><br/>                     | <span data-ttu-id="826a8-153">Требуется для подписки на уведомления.</span><span class="sxs-lookup"><span data-stu-id="826a8-153">Required to subscribe for notifications.</span></span> <span data-ttu-id="826a8-154">Подписчики будут получать уведомления только об объектах, к которым у них есть ФВПМ \_ актрл \_ доступ на чтение.</span><span class="sxs-lookup"><span data-stu-id="826a8-154">Subscribers will only receive notifications for objects to which they have FWPM\_ACTRL\_READ access.</span></span><br/>                 |
| <span data-ttu-id="826a8-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**ФВПМ \_ актрл \_ запись**</span><span class="sxs-lookup"><span data-stu-id="826a8-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span><br/>                                 | <span data-ttu-id="826a8-156">Требуется для установки параметров ядра.</span><span class="sxs-lookup"><span data-stu-id="826a8-156">Required to set engine options.</span></span><br/>                                                                                                                               |



 

<span data-ttu-id="826a8-157">BFE пропускает все проверки доступа для вызывающих объектов режима ядра.</span><span class="sxs-lookup"><span data-stu-id="826a8-157">BFE skips all access checks for kernel-mode callers.</span></span>

<span data-ttu-id="826a8-158">Чтобы запретить администраторам блокировку из BFE, членам встроенной группы «Администраторы» всегда предоставляется **фвпм \_ актрл \_ Open** для объекта Engine.</span><span class="sxs-lookup"><span data-stu-id="826a8-158">In order to prevent administrators from locking themselves out of BFE, members of the built-in administrators group are always granted **FWPM\_ACTRL\_OPEN** to the engine object.</span></span> <span data-ttu-id="826a8-159">Таким образом, администратор может восстановить доступ, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="826a8-159">Thus, an administrator can regain access through the following steps.</span></span>

-   <span data-ttu-id="826a8-160">Включите привилегию **SE \_ Take \_ Ownership \_ Name** .</span><span class="sxs-lookup"><span data-stu-id="826a8-160">Enable the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="826a8-161">Вызовите [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="826a8-161">Call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span> <span data-ttu-id="826a8-162">Вызов выполняется, так как участник является членом встроенных администраторов.</span><span class="sxs-lookup"><span data-stu-id="826a8-162">The call succeeds because the caller is a member of Built-in Administrators.</span></span>
-   <span data-ttu-id="826a8-163">Стать владельцем объекта Engine.</span><span class="sxs-lookup"><span data-stu-id="826a8-163">Take ownership of the engine object.</span></span> <span data-ttu-id="826a8-164">Это происходит успешно, так как у вызывающего объекта есть привилегия **SE \_ Take \_ Ownership \_ Name** .</span><span class="sxs-lookup"><span data-stu-id="826a8-164">This succeeds because the caller has the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="826a8-165">Обновите список DACL.</span><span class="sxs-lookup"><span data-stu-id="826a8-165">Update the DACL.</span></span> <span data-ttu-id="826a8-166">Это происходит успешно, так как владелец всегда имеет доступ на **запись \_ DAC** .</span><span class="sxs-lookup"><span data-stu-id="826a8-166">This succeeds because the owner always has **WRITE\_DAC** access</span></span>

<span data-ttu-id="826a8-167">Так как BFE поддерживает собственный пользовательский аудит, он не создает аудиты доступа к универсальным объектам.</span><span class="sxs-lookup"><span data-stu-id="826a8-167">Since BFE supports its own custom auditing, it does not generate generic object access audits.</span></span> <span data-ttu-id="826a8-168">Таким же списком SACL игнорируется.</span><span class="sxs-lookup"><span data-stu-id="826a8-168">Thus, the SACL is ignored.</span></span>

## <a name="wfp-required-access-rights"></a><span data-ttu-id="826a8-169">Необходимые права доступа в WFP</span><span class="sxs-lookup"><span data-stu-id="826a8-169">WFP Required Access Rights</span></span>

<span data-ttu-id="826a8-170">В приведенной ниже таблице показаны права доступа, необходимые функциям WFP для доступа к различным объектам платформы фильтрации.</span><span class="sxs-lookup"><span data-stu-id="826a8-170">The table below shows the access rights required by the WFP functions in order to access various filtering platform objects.</span></span> <span data-ttu-id="826a8-171">**Функции фвпмфилтер \* *_ перечислены в качестве примера для доступа к стандартным объектам. Все остальные функции, обращающиеся к стандартным объектам, следуют* \*** модели доступа к функциям _ фвпмфилтер.</span><span class="sxs-lookup"><span data-stu-id="826a8-171">The **FwpmFilter\**_ functions are listed as an example for accessing the standard objects. All the other functions that access standard objects follow the _\* FwpmFilter\**\* functions access model.</span></span>



<span data-ttu-id="826a8-172">Функция</span><span class="sxs-lookup"><span data-stu-id="826a8-172">Function</span></span>

<span data-ttu-id="826a8-173">Объект проверен</span><span class="sxs-lookup"><span data-stu-id="826a8-173">Object Checked</span></span>

<span data-ttu-id="826a8-174">Требуемый доступ</span><span class="sxs-lookup"><span data-stu-id="826a8-174">Access Required</span></span>

[<span data-ttu-id="826a8-175">**FwpmEngineOpen0**</span><span class="sxs-lookup"><span data-stu-id="826a8-175">**FwpmEngineOpen0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

<span data-ttu-id="826a8-176">Подсистема</span><span class="sxs-lookup"><span data-stu-id="826a8-176">Engine</span></span>

<span data-ttu-id="826a8-177">**ФВПМ \_ актрл \_ Open**</span><span class="sxs-lookup"><span data-stu-id="826a8-177">**FWPM\_ACTRL\_OPEN**</span></span>

[<span data-ttu-id="826a8-178">**FwpmEngineGetOption0**</span><span class="sxs-lookup"><span data-stu-id="826a8-178">**FwpmEngineGetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

<span data-ttu-id="826a8-179">Подсистема</span><span class="sxs-lookup"><span data-stu-id="826a8-179">Engine</span></span>

<span data-ttu-id="826a8-180">**\_Чтение фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-180">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="826a8-181">**FwpmEngineSetOption0**</span><span class="sxs-lookup"><span data-stu-id="826a8-181">**FwpmEngineSetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

<span data-ttu-id="826a8-182">Подсистема</span><span class="sxs-lookup"><span data-stu-id="826a8-182">Engine</span></span>

<span data-ttu-id="826a8-183">**ФВПМ \_ актрл \_ запись**</span><span class="sxs-lookup"><span data-stu-id="826a8-183">**FWPM\_ACTRL\_WRITE**</span></span>

[<span data-ttu-id="826a8-184">**FwpmSessionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="826a8-184">**FwpmSessionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

<span data-ttu-id="826a8-185">Подсистема</span><span class="sxs-lookup"><span data-stu-id="826a8-185">Engine</span></span>

<span data-ttu-id="826a8-186">**\_перечисление АКТРЛ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-186">**FWPM\_ACTRL\_ENUM**</span></span>

[<span data-ttu-id="826a8-187">**FwpmTransactionBegin0**</span><span class="sxs-lookup"><span data-stu-id="826a8-187">**FwpmTransactionBegin0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

<span data-ttu-id="826a8-188">Подсистема</span><span class="sxs-lookup"><span data-stu-id="826a8-188">Engine</span></span>

<span data-ttu-id="826a8-189">**Фвпм \_ актрл \_ начать \_ Чтение \_ транзакция**  &  **фвпм \_ актрл \_ начать \_ запись \_ транзакция**</span><span class="sxs-lookup"><span data-stu-id="826a8-189">**FWPM\_ACTRL\_BEGIN\_READ\_TXN** & **FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>

[<span data-ttu-id="826a8-190">**FwpmFilterAdd0**</span><span class="sxs-lookup"><span data-stu-id="826a8-190">**FwpmFilterAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

<span data-ttu-id="826a8-191">Поставщик контейнера</span><span class="sxs-lookup"><span data-stu-id="826a8-191">Container Provider</span></span><br/> <span data-ttu-id="826a8-192">Уровень</span><span class="sxs-lookup"><span data-stu-id="826a8-192">Layer</span></span><br/> <span data-ttu-id="826a8-193">Sub-Layer</span><span class="sxs-lookup"><span data-stu-id="826a8-193">Sub-Layer</span></span><br/> <span data-ttu-id="826a8-194">Выноска</span><span class="sxs-lookup"><span data-stu-id="826a8-194">Callout</span></span><br/> <span data-ttu-id="826a8-195">Контекст поставщика</span><span class="sxs-lookup"><span data-stu-id="826a8-195">Provider Context</span></span><br/>

<span data-ttu-id="826a8-196">**ФВПМ \_ актрл \_ аддфвпм \_ актрл \_ Add \_ Link**</span><span class="sxs-lookup"><span data-stu-id="826a8-196">**FWPM\_ACTRL\_ADDFWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="826a8-197">**ФВПМ \_ актрл \_ Добавить \_ ссылку**</span><span class="sxs-lookup"><span data-stu-id="826a8-197">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="826a8-198">**ФВПМ \_ актрл \_ Добавить \_ ссылку**</span><span class="sxs-lookup"><span data-stu-id="826a8-198">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="826a8-199">**ФВПМ \_ актрл \_ Добавить \_ ссылку**</span><span class="sxs-lookup"><span data-stu-id="826a8-199">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="826a8-200">**ФВПМ \_ актрл \_ Добавить \_ ссылку**</span><span class="sxs-lookup"><span data-stu-id="826a8-200">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>

<span data-ttu-id="826a8-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="826a8-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span></span><br/>

<span data-ttu-id="826a8-202">Фильтр</span><span class="sxs-lookup"><span data-stu-id="826a8-202">Filter</span></span>

<span data-ttu-id="826a8-203">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="826a8-203">**DELETE**</span></span>

<span data-ttu-id="826a8-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span><span class="sxs-lookup"><span data-stu-id="826a8-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span></span><br/>

<span data-ttu-id="826a8-205">Фильтр</span><span class="sxs-lookup"><span data-stu-id="826a8-205">Filter</span></span>

<span data-ttu-id="826a8-206">**\_Чтение фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-206">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="826a8-207">**FwpmFilterCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="826a8-207">**FwpmFilterCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

<span data-ttu-id="826a8-208">Фильтр контейнера</span><span class="sxs-lookup"><span data-stu-id="826a8-208">Container Filter</span></span><br/>

<span data-ttu-id="826a8-209">**ФВПМ \_ актрл \_ енумфвпм \_ актрл \_ Read**</span><span class="sxs-lookup"><span data-stu-id="826a8-209">**FWPM\_ACTRL\_ENUMFWPM\_ACTRL\_READ**</span></span><br/>

[<span data-ttu-id="826a8-210">**FwpmFilterSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="826a8-210">**FwpmFilterSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

<span data-ttu-id="826a8-211">Контейнер</span><span class="sxs-lookup"><span data-stu-id="826a8-211">Container</span></span>

<span data-ttu-id="826a8-212">**\_Подписка фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-212">**FWPM\_ACTRL\_SUBSCRIBE**</span></span>

[<span data-ttu-id="826a8-213">**FwpmFilterSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="826a8-213">**FwpmFilterSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

<span data-ttu-id="826a8-214">Контейнер</span><span class="sxs-lookup"><span data-stu-id="826a8-214">Container</span></span>

<span data-ttu-id="826a8-215">**\_Чтение фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-215">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="826a8-216">**IPsecGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="826a8-216">**IPsecGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

<span data-ttu-id="826a8-217">База данных SA IPsec</span><span class="sxs-lookup"><span data-stu-id="826a8-217">IPsec SA DB</span></span>

<span data-ttu-id="826a8-218">**\_ \_ Статистика чтения фвпм \_ актрл**</span><span class="sxs-lookup"><span data-stu-id="826a8-218">**FWPM\_ACTRL\_READ\_STATS**</span></span>

<span data-ttu-id="826a8-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span><span class="sxs-lookup"><span data-stu-id="826a8-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span></span><br/> [<span data-ttu-id="826a8-220">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="826a8-220">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [<span data-ttu-id="826a8-221">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="826a8-221">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

<span data-ttu-id="826a8-222">База данных SA IPsec</span><span class="sxs-lookup"><span data-stu-id="826a8-222">IPsec SA DB</span></span>

<span data-ttu-id="826a8-223">**\_Добавление фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-223">**FWPM\_ACTRL\_ADD**</span></span>

<span data-ttu-id="826a8-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span><span class="sxs-lookup"><span data-stu-id="826a8-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span></span><br/>

<span data-ttu-id="826a8-225">База данных SA IPsec</span><span class="sxs-lookup"><span data-stu-id="826a8-225">IPsec SA DB</span></span>

<span data-ttu-id="826a8-226">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="826a8-226">**DELETE**</span></span>

[<span data-ttu-id="826a8-227">**IPsecSaContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="826a8-227">**IPsecSaContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

<span data-ttu-id="826a8-228">База данных SA IPsec</span><span class="sxs-lookup"><span data-stu-id="826a8-228">IPsec SA DB</span></span>

<span data-ttu-id="826a8-229">**\_Чтение фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-229">**FWPM\_ACTRL\_READ**</span></span>

<span data-ttu-id="826a8-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span><span class="sxs-lookup"><span data-stu-id="826a8-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span></span><br/>

<span data-ttu-id="826a8-231">База данных SA IPsec</span><span class="sxs-lookup"><span data-stu-id="826a8-231">IPsec SA DB</span></span>

<span data-ttu-id="826a8-232">**Фвпм \_ актрл \_ enum**  &  **фвпм \_ актрл \_ Read**</span><span class="sxs-lookup"><span data-stu-id="826a8-232">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="826a8-233">**IkeextGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="826a8-233">**IkeextGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

<span data-ttu-id="826a8-234">БАЗА ДАННЫХ IKE SA</span><span class="sxs-lookup"><span data-stu-id="826a8-234">IKE SA DB</span></span>

<span data-ttu-id="826a8-235">**\_ \_ Статистика чтения фвпм \_ актрл**</span><span class="sxs-lookup"><span data-stu-id="826a8-235">**FWPM\_ACTRL\_READ\_STATS**</span></span>

[<span data-ttu-id="826a8-236">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="826a8-236">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

<span data-ttu-id="826a8-237">БАЗА ДАННЫХ IKE SA</span><span class="sxs-lookup"><span data-stu-id="826a8-237">IKE SA DB</span></span>

<span data-ttu-id="826a8-238">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="826a8-238">**DELETE**</span></span>

[<span data-ttu-id="826a8-239">**IkeextSaGetById0**</span><span class="sxs-lookup"><span data-stu-id="826a8-239">**IkeextSaGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

<span data-ttu-id="826a8-240">БАЗА ДАННЫХ IKE SA</span><span class="sxs-lookup"><span data-stu-id="826a8-240">IKE SA DB</span></span>

<span data-ttu-id="826a8-241">**\_Чтение фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-241">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="826a8-242">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="826a8-242">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

<span data-ttu-id="826a8-243">БАЗА ДАННЫХ IKE SA</span><span class="sxs-lookup"><span data-stu-id="826a8-243">IKE SA DB</span></span>

<span data-ttu-id="826a8-244">**Фвпм \_ актрл \_ enum**  &  **фвпм \_ актрл \_ Read**</span><span class="sxs-lookup"><span data-stu-id="826a8-244">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="826a8-245">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="826a8-245">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

<span data-ttu-id="826a8-246">Контейнер</span><span class="sxs-lookup"><span data-stu-id="826a8-246">Container</span></span>

<span data-ttu-id="826a8-247">**\_перечисление АКТРЛ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="826a8-247">**FWPM\_ACTRL\_ENUM**</span></span>

<span data-ttu-id="826a8-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="826a8-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span></span><br/>

<span data-ttu-id="826a8-249">Дополнительные проверки доступа выходят за рамки отдельных фильтров и контекстов поставщиков</span><span class="sxs-lookup"><span data-stu-id="826a8-249">No additional access checks beyond those for the individual filters and provider contexts</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="826a8-250">См. также</span><span class="sxs-lookup"><span data-stu-id="826a8-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="826a8-251">**Стандартные права доступа**</span><span class="sxs-lookup"><span data-stu-id="826a8-251">**Standard Access Rights**</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="826a8-252">Модель управления доступом Windows</span><span class="sxs-lookup"><span data-stu-id="826a8-252">Windows access control model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[<span data-ttu-id="826a8-253">**Идентификаторы прав доступа платформы фильтрации Windows**</span><span class="sxs-lookup"><span data-stu-id="826a8-253">**Windows Filtering Platform Access Rights Identifiers**</span></span>](access-right-identifiers.md)
</dt> </dl>

 

