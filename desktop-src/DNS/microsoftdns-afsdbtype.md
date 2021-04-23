---
title: Класс MicrosoftDNS_AFSDBType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись сервера базы данных AFS (AFSDB).
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- DNS класса MicrosoftDNS_AFSDBType
- DNS-MicrosoftDNS_AFSDBType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071640"
---
# <a name="microsoftdns_afsdbtype-class"></a><span data-ttu-id="dbe12-105">\_Класс микрософтднс афсдбтипе</span><span class="sxs-lookup"><span data-stu-id="dbe12-105">MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="dbe12-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись сервера базы данных AFS (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="dbe12-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an Andrew File System Database Server (AFSDB) record.</span></span>

<span data-ttu-id="dbe12-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="dbe12-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe12-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbe12-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a><span data-ttu-id="dbe12-109">Члены</span><span class="sxs-lookup"><span data-stu-id="dbe12-109">Members</span></span>

<span data-ttu-id="dbe12-110">Класс **микрософтднс \_ афсдбтипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dbe12-110">The **MicrosoftDNS\_AFSDBType** class has these types of members:</span></span>

-   [<span data-ttu-id="dbe12-111">Методы</span><span class="sxs-lookup"><span data-stu-id="dbe12-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dbe12-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbe12-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dbe12-113">Методы</span><span class="sxs-lookup"><span data-stu-id="dbe12-113">Methods</span></span>

<span data-ttu-id="dbe12-114">Класс **микрософтднс \_ афсдбтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dbe12-114">The **MicrosoftDNS\_AFSDBType** class has these methods.</span></span>



| <span data-ttu-id="dbe12-115">Метод</span><span class="sxs-lookup"><span data-stu-id="dbe12-115">Method</span></span>                             | <span data-ttu-id="dbe12-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dbe12-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe12-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="dbe12-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="dbe12-118">Создает экземпляр записи ресурса AFSDB на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца/ячейки, класс (по умолчанию — IN), значение срока жизни, а также тип и имя узла сервера AFS.</span><span class="sxs-lookup"><span data-stu-id="dbe12-118">Instantiates an AFSDB Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Cell Name, class (default = IN), time-to-live value, and host AFS server subtype and name.</span></span> <span data-ttu-id="dbe12-119">Возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="dbe12-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="dbe12-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="dbe12-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="dbe12-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="dbe12-121">**Modify**</span></span>                         | <span data-ttu-id="dbe12-122">Этот метод обновляет значения TTL, подтип и имя сервера до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="dbe12-122">This method updates the TTL, Subtype and Server Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="dbe12-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="dbe12-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="dbe12-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="dbe12-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="dbe12-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="dbe12-125">Qualifiers: Implemented</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="dbe12-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbe12-126">Properties</span></span>

<span data-ttu-id="dbe12-127">Класс **микрософтднс \_ афсдбтипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dbe12-127">The **MicrosoftDNS\_AFSDBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbe12-128">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="dbe12-128">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbe12-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbe12-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbe12-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbe12-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbe12-131">Полное доменное имя, указывающее узел с сервером для ячейки AFS, указанной в имени владельца.</span><span class="sxs-lookup"><span data-stu-id="dbe12-131">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="dbe12-132">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="dbe12-132">**Subtype**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbe12-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbe12-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbe12-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbe12-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbe12-135">Подтип ведущего сервера AFS.</span><span class="sxs-lookup"><span data-stu-id="dbe12-135">Subtype of the host AFS server.</span></span> <span data-ttu-id="dbe12-136">Для подтипа 1 (значение 1) на узле имеется сервер AFS версии 3,0 для именованной ячейки AFS.</span><span class="sxs-lookup"><span data-stu-id="dbe12-136">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="dbe12-137">В случае подтипа 2 (значение = 2) узел имеет прошедший проверку подлинности сервер имен, в котором размещен узел корневого каталога ячеек для именованной ячейки DCE/NCA.</span><span class="sxs-lookup"><span data-stu-id="dbe12-137">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbe12-138">Требования</span><span class="sxs-lookup"><span data-stu-id="dbe12-138">Requirements</span></span>



| <span data-ttu-id="dbe12-139">Требование</span><span class="sxs-lookup"><span data-stu-id="dbe12-139">Requirement</span></span> | <span data-ttu-id="dbe12-140">Значение</span><span class="sxs-lookup"><span data-stu-id="dbe12-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe12-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbe12-141">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe12-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dbe12-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dbe12-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbe12-143">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe12-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbe12-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dbe12-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dbe12-145">Namespace</span></span><br/>                | <span data-ttu-id="dbe12-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="dbe12-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dbe12-147">MOF</span><span class="sxs-lookup"><span data-stu-id="dbe12-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbe12-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbe12-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe12-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbe12-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe12-150">**Метод Креатеинстанцефромпропертидата \_ класса Афсдбтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="dbe12-150">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="dbe12-151">**Метод Modify \_ класса микрософтднс афсдбтипе**</span><span class="sxs-lookup"><span data-stu-id="dbe12-151">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="dbe12-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="dbe12-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





