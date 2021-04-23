---
description: Тип данных, используемый для указания атрибутов доступа безопасности в реестре.
title: РЕГСАМ (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987605"
---
# <a name="regsam"></a><span data-ttu-id="85441-103">регсам</span><span class="sxs-lookup"><span data-stu-id="85441-103">REGSAM</span></span>

<span data-ttu-id="85441-104">Тип данных, используемый для указания атрибутов доступа безопасности в реестре.</span><span class="sxs-lookup"><span data-stu-id="85441-104">A data type used for specifying the security access attributes in the registry.</span></span>



| <span data-ttu-id="85441-105">Константа</span><span class="sxs-lookup"><span data-stu-id="85441-105">Constant</span></span>                                                                                                                                                                                   | <span data-ttu-id="85441-106">Описание</span><span class="sxs-lookup"><span data-stu-id="85441-106">Description</span></span>                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <span data-ttu-id="85441-107"><dt>**КЛЮЧЕВОЙ \_ полный \_ доступ**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-107"><dt>**KEY\_ALL\_ACCESS**</dt></span></span> </dl>                          | <span data-ttu-id="85441-108">Сочетание \* \* \* \* ключ \_ запроса \_ значения \* \* \* \*, \* \* \* \* ключ \_ перечисляет \_ \_ подразделы \* \* \* \*, \* \* \* \* \_ уведомление о ключе \* \* \* \*, \* \* \* \* \_ ключ \_ создания \_ подраздела \* \* \_ \_ \_ \_ \* \*, \* \* \* \* ключ создания ссылки \* \* \* \* и \* \* \* \* \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="85441-108">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, \*\*\*\*KEY\_NOTIFY\*\*\*\*, \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\*, \*\*\*\*KEY\_CREATE\_LINK\*\*\*\*, and \*\*\*\*KEY\_SET\_VALUE\*\*\*\* access.</span></span><br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <span data-ttu-id="85441-109"><dt>**\_ссылка для создания ключа \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-109"><dt>**KEY\_CREATE\_LINK**</dt></span></span> </dl>                       | <span data-ttu-id="85441-110">Разрешение на создание символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="85441-110">Permission to create a symbolic link.</span></span><br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <span data-ttu-id="85441-111"><dt>**ключ \_ создания \_ ключа \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-111"><dt>**KEY\_CREATE\_SUB\_KEY**</dt></span></span> </dl>             | <span data-ttu-id="85441-112">Разрешение на создание подразделов.</span><span class="sxs-lookup"><span data-stu-id="85441-112">Permission to create subkeys.</span></span><br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <span data-ttu-id="85441-113"><dt>**КЛЮЧ, \_ Перечисление \_ вложенных \_ ключей**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-113"><dt>**KEY\_ENUMERATE\_SUB\_KEYS**</dt></span></span> </dl> | <span data-ttu-id="85441-114">Разрешение на перечисление подразделов.</span><span class="sxs-lookup"><span data-stu-id="85441-114">Permission to enumerate subkeys.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <span data-ttu-id="85441-115"><dt>**\_выполнение ключа**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-115"><dt>**KEY\_EXECUTE**</dt></span></span> </dl>                                    | <span data-ttu-id="85441-116">Разрешение на доступ для чтения.</span><span class="sxs-lookup"><span data-stu-id="85441-116">Permission for read access.</span></span><br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <span data-ttu-id="85441-117"><dt>**\_уведомление ключа**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-117"><dt>**KEY\_NOTIFY**</dt></span></span> </dl>                                       | <span data-ttu-id="85441-118">Разрешение на уведомление об изменении.</span><span class="sxs-lookup"><span data-stu-id="85441-118">Permission for change notification.</span></span><br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <span data-ttu-id="85441-119"><dt>**значение КЛЮЧЕВого \_ запроса \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-119"><dt>**KEY\_QUERY\_VALUE**</dt></span></span> </dl>                       | <span data-ttu-id="85441-120">Разрешение на запрос данных подраздела.</span><span class="sxs-lookup"><span data-stu-id="85441-120">Permission to query subkey data.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <span data-ttu-id="85441-121"><dt>**\_чтение ключа**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-121"><dt>**KEY\_READ**</dt></span></span> </dl>                                             | <span data-ttu-id="85441-122">Сочетание \* \* \* \* ключ \_ запроса \_ значения \* \* \* \*, \* \* \* \* ключ \_ перечисляет \_ \_ подразделы \* \* \* \* и \* \* \* \* \_ уведомление о ключе \* \* \* \* доступ.</span><span class="sxs-lookup"><span data-stu-id="85441-122">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, and \*\*\*\*KEY\_NOTIFY\*\*\*\* access.</span></span><br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <span data-ttu-id="85441-123"><dt>**\_значение набора \_ ключей**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-123"><dt>**KEY\_SET\_VALUE**</dt></span></span> </dl>                             | <span data-ttu-id="85441-124">Разрешение на установку данных подраздела.</span><span class="sxs-lookup"><span data-stu-id="85441-124">Permission to set subkey data.</span></span><br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <span data-ttu-id="85441-125"><dt>**\_запись ключа**</dt></span><span class="sxs-lookup"><span data-stu-id="85441-125"><dt>**KEY\_WRITE**</dt></span></span> </dl>                                          | <span data-ttu-id="85441-126">Сочетание \* \* \* \* \_ значения набора ключей \_ \* \* \* \* и \* \* \* \* ключ \_ создания \_ \_ подраздела \* \* \* \* Access.</span><span class="sxs-lookup"><span data-stu-id="85441-126">Combination of \*\*\*\*KEY\_SET\_VALUE\*\*\*\* and \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\* access.</span></span><br/>                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="85441-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="85441-127">Remarks</span></span>

<span data-ttu-id="85441-128">Значение **регсам** может быть одним или несколькими перечисляемыми значениями.</span><span class="sxs-lookup"><span data-stu-id="85441-128">A **REGSAM** value can be one or more of the listed values.</span></span>

## <a name="requirements"></a><span data-ttu-id="85441-129">Требования</span><span class="sxs-lookup"><span data-stu-id="85441-129">Requirements</span></span>



| <span data-ttu-id="85441-130">Требование</span><span class="sxs-lookup"><span data-stu-id="85441-130">Requirement</span></span> | <span data-ttu-id="85441-131">Значение</span><span class="sxs-lookup"><span data-stu-id="85441-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85441-132">Header</span><span class="sxs-lookup"><span data-stu-id="85441-132">Header</span></span><br/> | <dl> <span data-ttu-id="85441-133"><dt>Файл Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="85441-133"><dt>Winnt.h</dt></span></span> </dl> |



 

 




