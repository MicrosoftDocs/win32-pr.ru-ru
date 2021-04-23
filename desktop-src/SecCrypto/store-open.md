---
description: Открывает указанное хранилище сертификатов.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Метод Store. Open
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665452"
---
# <a name="storeopen-method"></a><span data-ttu-id="e56ec-103">Метод Store. Open</span><span class="sxs-lookup"><span data-stu-id="e56ec-103">Store.Open method</span></span>

<span data-ttu-id="e56ec-104">\[Метод **Open** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e56ec-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e56ec-105">Вместо этого используйте [**класс X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e56ec-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e56ec-106">Метод **Open** открывает указанное [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e56ec-106">The **Open** method opens a specified [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="e56ec-107">По умолчанию \_ \_ расположение хранилища CAPICOM Current User \_ и хранилище CAPICOM \_ My \_ Store открываются только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e56ec-107">By default, the CAPICOM\_CURRENT\_USER\_STORE location and CAPICOM\_MY\_STORE store are opened as read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56ec-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e56ec-108">Syntax</span></span>


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e56ec-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e56ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e56ec-110">*StoreLocation* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e56ec-110">*StoreLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e56ec-111">Значение перечисления [CAPICOM \_ \_ Location](capicom-store-location.md) , указывающее расположение открываемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="e56ec-111">A value of the [CAPICOM\_STORE\_LOCATION](capicom-store-location.md) enumeration that indicates the location of the store to be opened.</span></span> <span data-ttu-id="e56ec-112">Значение по умолчанию — "CAPICOM \_ Current \_ user \_ Store".</span><span class="sxs-lookup"><span data-stu-id="e56ec-112">The default value is CAPICOM\_CURRENT\_USER\_STORE.</span></span> <span data-ttu-id="e56ec-113">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="e56ec-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e56ec-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-114">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="e56ec-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-115">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <span data-ttu-id="e56ec-116"><dt>**CAPICOM \_ Active \_ Directory \_ пользовательское \_ хранилище**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-116"><dt>**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="e56ec-117">Магазин является хранилищем Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e56ec-117">The store is an Active Directory store.</span></span> <span data-ttu-id="e56ec-118">Если хранилище Active Directory открыто как доступное для чтения и записи, то ошибка не будет сформирована, но любые изменения в хранилище не будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="e56ec-118">No error will be generated if an Active Directory store is opened as read/write, but any changes to the store will not be persisted.</span></span> <span data-ttu-id="e56ec-119">Сертификаты нельзя добавлять в хранилища Active Directory или удалять из них.</span><span class="sxs-lookup"><span data-stu-id="e56ec-119">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <span data-ttu-id="e56ec-120"><dt>**\_хранилище CAPICOM текущего \_ пользователя \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-120"><dt>**CAPICOM\_CURRENT\_USER\_STORE**</dt></span></span> </dl>                             | <span data-ttu-id="e56ec-121">Хранилище является хранилищем текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="e56ec-121">The store is a current user store.</span></span> <span data-ttu-id="e56ec-122">Хранилище текущего пользователя может быть хранилищем для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e56ec-122">A current user store may be a read/write store.</span></span> <span data-ttu-id="e56ec-123">Если это так, изменения в содержимом хранилища сохраняются.</span><span class="sxs-lookup"><span data-stu-id="e56ec-123">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <span data-ttu-id="e56ec-124"><dt>**хранилище CAPICOM на \_ локальном \_ компьютере \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-124"><dt>**CAPICOM\_LOCAL\_MACHINE\_STORE**</dt></span></span> </dl>                          | <span data-ttu-id="e56ec-125">Это хранилище локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="e56ec-125">The store is a local computer store.</span></span> <span data-ttu-id="e56ec-126">Хранилища локальных компьютеров могут быть хранилищами для чтения и записи только в том случае, если у пользователя есть разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e56ec-126">Local computer stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="e56ec-127">Если у пользователя есть разрешения на чтение и запись и если хранилище открыто для чтения и записи, то изменения в содержимом хранилища сохраняются.</span><span class="sxs-lookup"><span data-stu-id="e56ec-127">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <span data-ttu-id="e56ec-128"><dt>**\_хранилище CAPICOM Memory \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-128"><dt>**CAPICOM\_MEMORY\_STORE**</dt></span></span> </dl>                                                | <span data-ttu-id="e56ec-129">Хранилище является хранилищем памяти.</span><span class="sxs-lookup"><span data-stu-id="e56ec-129">The store is a memory store.</span></span> <span data-ttu-id="e56ec-130">Любые изменения в содержимом хранилища не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="e56ec-130">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <span data-ttu-id="e56ec-131"><dt>**\_хранилище CAPICOM смарт- \_ карты \_ пользователя \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-131"><dt>**CAPICOM\_SMART\_CARD\_USER\_STORE**</dt></span></span> </dl>                   | <span data-ttu-id="e56ec-132">Магазин — это группа существующих смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="e56ec-132">The store is the group of present smart cards.</span></span> <span data-ttu-id="e56ec-133">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e56ec-133">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="e56ec-134">*StoreName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e56ec-134">*StoreName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e56ec-135">Строка, содержащая имя системного хранилища сертификатов, которое необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="e56ec-135">A string that contains the name of the system certificate store to be opened.</span></span> <span data-ttu-id="e56ec-136">Значение по умолчанию — CAPICOM \_ My \_ Store.</span><span class="sxs-lookup"><span data-stu-id="e56ec-136">The default value is CAPICOM\_MY\_STORE.</span></span> <span data-ttu-id="e56ec-137">Если хранилище открывается из веб-скрипта, \\ в имени не может использоваться символ обратной косой черты ().</span><span class="sxs-lookup"><span data-stu-id="e56ec-137">If the store is opened from a web script, the backslash (\\) character is not allowed in the name.</span></span> <span data-ttu-id="e56ec-138">В дополнение к хранилищам, определенным системой, можно открыть пользовательские хранилища.</span><span class="sxs-lookup"><span data-stu-id="e56ec-138">In addition to stores defined by the system, user-defined stores can be opened.</span></span>

<span data-ttu-id="e56ec-139">Этот параметр может быть определяемым пользователем хранилищем или одним из следующих системных хранилищ сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e56ec-139">This parameter can be a user-defined store or one of the following system certificate stores.</span></span>



| <span data-ttu-id="e56ec-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-140">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="e56ec-141">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-141">Meaning</span></span>                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <span data-ttu-id="e56ec-142"><dt>**\_хранилище CAPICOM CA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-142"><dt>**CAPICOM\_CA\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="e56ec-143">Хранилище CA.</span><span class="sxs-lookup"><span data-stu-id="e56ec-143">CA store.</span></span> <span data-ttu-id="e56ec-144">Это хранилище используется для хранения промежуточных сертификатов ЦС.</span><span class="sxs-lookup"><span data-stu-id="e56ec-144">This store is used to store intermediate CA certificates.</span></span><br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <span data-ttu-id="e56ec-145"><dt>**CAPICOM \_ My \_ Store**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-145"><dt>**CAPICOM\_MY\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="e56ec-146">Мое хранилище.</span><span class="sxs-lookup"><span data-stu-id="e56ec-146">My store.</span></span> <span data-ttu-id="e56ec-147">Это хранилище используется для персональных сертификатов пользователя.</span><span class="sxs-lookup"><span data-stu-id="e56ec-147">This store is used for a user's personal certificates.</span></span><br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <span data-ttu-id="e56ec-148"><dt>**CAPICOM \_ другое \_ хранилище**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-148"><dt>**CAPICOM\_OTHER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="e56ec-149">Хранилище AddressBook.</span><span class="sxs-lookup"><span data-stu-id="e56ec-149">AddressBook store.</span></span> <span data-ttu-id="e56ec-150">Это хранилище используется для хранения сертификатов других пользователей.</span><span class="sxs-lookup"><span data-stu-id="e56ec-150">This store is used to keep the certificates of others.</span></span><br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <span data-ttu-id="e56ec-151"><dt>**\_корневое \_ хранилище CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-151"><dt>**CAPICOM\_ROOT\_STORE**</dt></span></span> </dl>    | <span data-ttu-id="e56ec-152">Корневое хранилище.</span><span class="sxs-lookup"><span data-stu-id="e56ec-152">Root store.</span></span> <span data-ttu-id="e56ec-153">Это хранилище используется для хранения корневого ЦС и самозаверяющих доверенных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e56ec-153">This store is used to store the root CA and self-signed, trusted certificates.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e56ec-154">*OpenMode* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e56ec-154">*OpenMode* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e56ec-155">Значение перечисления в [ \_ \_ открытом \_ режиме CAPICOM Store](capicom-store-open-mode.md) , указывающее режим открытия хранилища.</span><span class="sxs-lookup"><span data-stu-id="e56ec-155">A value of the [CAPICOM\_STORE\_OPEN\_MODE](capicom-store-open-mode.md) enumeration that indicates the open mode of the store.</span></span> <span data-ttu-id="e56ec-156">Значение по умолчанию — CAPICOM \_ Store \_ открыть только для \_ чтения \_ .</span><span class="sxs-lookup"><span data-stu-id="e56ec-156">The default value is CAPICOM\_STORE\_OPEN\_READ\_ONLY.</span></span> <span data-ttu-id="e56ec-157">Если хранилище открывается из веб-скрипта, это значение принудительно устанавливается в режим \_ CAPICOM \_ Store \_ открыть \_ только существующий.</span><span class="sxs-lookup"><span data-stu-id="e56ec-157">If the store is opened from a web script, this value is forced to CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY.</span></span> <span data-ttu-id="e56ec-158">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="e56ec-158">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e56ec-159">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-159">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="e56ec-160">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-160">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <span data-ttu-id="e56ec-161"><dt>**\_ \_ \_ Максимальное \_ допустимое число открытых в CAPICOM Store**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-161"><dt>**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</dt></span></span> </dl> | <span data-ttu-id="e56ec-162">Откройте хранилище в режиме чтения и записи, если пользователь имеет разрешения на чтение и запись. в противном случае откройте хранилище в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e56ec-162">Open the store in read/write mode if the user has read/write permissions; otherwise, open the store in read-only mode.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <span data-ttu-id="e56ec-163"><dt>**CAPICOM \_ Store \_ открыт \_ только для чтения \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-163"><dt>**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</dt></span></span> </dl>                   | <span data-ttu-id="e56ec-164">Откройте хранилище в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e56ec-164">Open the store in read-only mode.</span></span><br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <span data-ttu-id="e56ec-165"><dt>**CAPICOM \_ Store \_ открыть \_ чтение и \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-165"><dt>**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</dt></span></span> </dl>                | <span data-ttu-id="e56ec-166">Откройте хранилище в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e56ec-166">Open the store in read/write mode.</span></span><br/>                                                                                     |



 

<span data-ttu-id="e56ec-167">Следующие флаги можно объединять со значениями из предыдущей таблицы с помощью операции логического **или** .</span><span class="sxs-lookup"><span data-stu-id="e56ec-167">The following flags can be combined with the values in the previous table by using a logical-**OR** operation.</span></span>



| <span data-ttu-id="e56ec-168">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-168">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="e56ec-169">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-169">Meaning</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <span data-ttu-id="e56ec-170"><dt>**в \_ CAPICOM \_ Store \_ открыто \_ только существующее**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-170"><dt>**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</dt></span></span> </dl>          | <span data-ttu-id="e56ec-171">Открывать только существующие магазины; не создавать новое хранилище.</span><span class="sxs-lookup"><span data-stu-id="e56ec-171">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="e56ec-172">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e56ec-172">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <span data-ttu-id="e56ec-173"><dt>**\_открыто хранилище CAPICOM, \_ \_ включая \_ архивированные**</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-173"><dt>**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</dt></span></span> </dl> | <span data-ttu-id="e56ec-174">Включать архивные сертификаты при использовании хранилища.</span><span class="sxs-lookup"><span data-stu-id="e56ec-174">Include archived certificates when using the store.</span></span> <span data-ttu-id="e56ec-175">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e56ec-175">Introduced in CAPICOM 2.0.</span></span><br/>   |



 

<span data-ttu-id="e56ec-176">Хранилища в некоторых местах можно открывать только в режиме "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="e56ec-176">Stores in some locations can be opened only in read-only mode.</span></span> <span data-ttu-id="e56ec-177">К ним относятся все магазины в \_ \_ хранилище CAPICOM \_ , для которых у пользователя нет разрешений на запись.</span><span class="sxs-lookup"><span data-stu-id="e56ec-177">These include all stores in CAPICOM\_LOCAL\_MACHINE\_STORE for which the user does not have write permissions.</span></span> <span data-ttu-id="e56ec-178">Попытки открыть хранилище в качестве хранилища для чтения и записи без правильного доступа и разрешений приведут к сбою метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="e56ec-178">Attempts to open a store as a read/write store without proper access and permissions will result in the failure of the **Open** method.</span></span> <span data-ttu-id="e56ec-179">Хранилища Active Directory можно открыть как хранилище для чтения и записи без сбоя метода **Open** , но изменения в хранилище не будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="e56ec-179">Active Directory stores can be opened as a read/write store without failure of the **Open** method, but changes to the store will not be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e56ec-180">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-180">Return value</span></span>

<span data-ttu-id="e56ec-181">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e56ec-181">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e56ec-182">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e56ec-182">Remarks</span></span>

<span data-ttu-id="e56ec-183">Если этот метод вызывается в хранилище смарт-карты, можно вызвать дополнительные пользовательские интерфейсы смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="e56ec-183">If this method is called on a SmartCard store, additional SmartCard user interfaces may be invoked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e56ec-184">При вызове этого метода из веб-скрипта сценарий должен получить доступ к цифровым сертификатам на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e56ec-184">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="e56ec-185">Если разрешить сценарию доступ к цифровым сертификатам, веб-сайт, с которого выполняется сценарий, также будет получать доступ к личным сведениям, хранящимся в сертификатах.</span><span class="sxs-lookup"><span data-stu-id="e56ec-185">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="e56ec-186">При первом вызове этого метода из определенного домена создается диалоговое окно, в котором пользователь должен указать, следует ли разрешить доступ к сертификатам.</span><span class="sxs-lookup"><span data-stu-id="e56ec-186">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span> <span data-ttu-id="e56ec-187">Хранилища, открытые из веб-скрипта, автоматически принудительно применяют \_ флаг CAPICOM Store \_ открыть \_ \_ только существующий.</span><span class="sxs-lookup"><span data-stu-id="e56ec-187">Stores opened from a web script automatically force the CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY flag.</span></span>

 

<span data-ttu-id="e56ec-188">Если *StoreLocation* является **\_ \_ \_ пользовательским \_ хранилищем CAPICOM смарт-карты**, *StoreName* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e56ec-188">If *StoreLocation* is **CAPICOM\_SMART\_CARD\_USER\_STORE**, *StoreName* is ignored.</span></span> <span data-ttu-id="e56ec-189">В этом случае CAPICOM считывает все сертификаты из всех доступных читателей, содержащих смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="e56ec-189">In this case, CAPICOM reads all certificates from all available readers that contain a smart card.</span></span>

## <a name="requirements"></a><span data-ttu-id="e56ec-190">Требования</span><span class="sxs-lookup"><span data-stu-id="e56ec-190">Requirements</span></span>



| <span data-ttu-id="e56ec-191">Требование</span><span class="sxs-lookup"><span data-stu-id="e56ec-191">Requirement</span></span> | <span data-ttu-id="e56ec-192">Значение</span><span class="sxs-lookup"><span data-stu-id="e56ec-192">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e56ec-193">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e56ec-193">Redistributable</span></span><br/> | <span data-ttu-id="e56ec-194">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e56ec-194">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e56ec-195">DLL</span><span class="sxs-lookup"><span data-stu-id="e56ec-195">DLL</span></span><br/>             | <dl> <span data-ttu-id="e56ec-196"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e56ec-196"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56ec-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e56ec-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56ec-198">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="e56ec-198">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="e56ec-199">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="e56ec-199">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="e56ec-200">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="e56ec-200">**Close**</span></span>](store-close.md)
</dt> </dl>

 

 
