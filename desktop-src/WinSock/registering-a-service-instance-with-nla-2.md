---
description: Клиенты NLA могут записывать сведения о конфигурации сети на уровне всей системы, что позволяет будущим запросам возвращать указанные сведения о конфигурации независимо от того, активна ли сеть.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Регистрация экземпляра службы с помощью NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692838"
---
# <a name="registering-a-service-instance-with-nla"></a><span data-ttu-id="9376a-103">Регистрация экземпляра службы с помощью NLA</span><span class="sxs-lookup"><span data-stu-id="9376a-103">Registering a Service Instance with NLA</span></span>

<span data-ttu-id="9376a-104">Клиенты NLA могут записывать сведения о конфигурации сети на уровне всей системы, что позволяет будущим запросам возвращать указанные сведения о конфигурации независимо от того, активна ли сеть.</span><span class="sxs-lookup"><span data-stu-id="9376a-104">NLA clients can record network configuration information on a system-wide basis, enabling future queries to return the specified configuration information regardless of whether the network is active.</span></span> <span data-ttu-id="9376a-105">Эта возможность позволяет клиентам NLA влиять на согласованное взаимодействие с данными о сети в нескольких приложениях.</span><span class="sxs-lookup"><span data-stu-id="9376a-105">This capability allows NLA clients to affect a consistent network information user experience across multiple applications.</span></span>

## <a name="parameters"></a><span data-ttu-id="9376a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9376a-106">Parameters</span></span>

<span data-ttu-id="9376a-107">Чтобы зарегистрировать экземпляр службы в поставщике службы сетевого расположения, используйте функцию [**всасетсервице**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) .</span><span class="sxs-lookup"><span data-stu-id="9376a-107">To register a service instance with the Network Location Awareness service provider, use the [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function.</span></span> <span data-ttu-id="9376a-108">Для правильной регистрации экземпляра службы некоторые параметры функции **всасетсервице** должны быть установлены с соответствующей информацией, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="9376a-108">In order to properly register a service instance certain parameters of the **WSASetService** function must be set with the appropriate information, as explained in this section.</span></span> <span data-ttu-id="9376a-109">Для краткого справочника функция **всасетсервице** имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="9376a-109">For quick reference, the **WSASetService** function has the following syntax:</span></span>

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

<span data-ttu-id="9376a-110">Для параметра *лпксрегинфо* предоставьте структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) из результата запроса NLA SP или соблюдайте требования запроса NLA SP, как указано в [запросе NLA](querying-nla-2.md).</span><span class="sxs-lookup"><span data-stu-id="9376a-110">For the *lpqsRegInfo* parameter, provide a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure from either an NLA SP query result, or constructed adhering to the requirements of an NLA SP query, as specified in [Querying NLA](querying-nla-2.md).</span></span>

<span data-ttu-id="9376a-111">Для параметра *ессоператион* поддерживаются следующие операции:</span><span class="sxs-lookup"><span data-stu-id="9376a-111">Operations supported for the *essOperation* parameter are the following:</span></span>

<dl> <dt>

<span data-ttu-id="9376a-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>РНРСЕРВИЦЕ \_ регистр</span><span class="sxs-lookup"><span data-stu-id="9376a-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE\_REGISTER</span></span>
</dt> <dd>

<span data-ttu-id="9376a-113">Сеть, определенная в структуре [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , предоставленной в *лпксрегинфо* , становится постоянной для активного пользователя путем сохранения экземпляра сети в кусте реестра для текущего пользователя, что позволяет выполнять олицетворение.</span><span class="sxs-lookup"><span data-stu-id="9376a-113">The network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is made persistent for the active user by storing the network instance in the registry hive for the current user, which allows impersonation.</span></span>

</dd> <dt>

<span data-ttu-id="9376a-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>РНРСЕРВИЦЕ \_ Удаление</span><span class="sxs-lookup"><span data-stu-id="9376a-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE\_DELETE</span></span>
</dt> <dd>

<span data-ttu-id="9376a-115">Если сеть, определенная в структуре [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , предоставленной в *лпксрегинфо* , является постоянной, она будет удалена.</span><span class="sxs-lookup"><span data-stu-id="9376a-115">If the network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is persistent, it will be removed.</span></span>

</dd> </dl>

<span data-ttu-id="9376a-116">Операция, указанная в параметре *ессоператион* , может быть изменена следующими параметрами, которые можно указать с помощью бинарной или логики:</span><span class="sxs-lookup"><span data-stu-id="9376a-116">The operation specified in the *essOperation* parameter can be modified by the following options, which can be specified with binary OR logic:</span></span>

<dl> <dt>

<span data-ttu-id="9376a-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_понятное \_ имя NLA</span><span class="sxs-lookup"><span data-stu-id="9376a-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA\_FRIENDLY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="9376a-118">При использовании с РНРСЕРВИЦЕ \_ Register поле *лпсзкоммент* сети, определенной в *лпксрегинфо* , проверяется на допустимость и сохраняется в постоянном состоянии.</span><span class="sxs-lookup"><span data-stu-id="9376a-118">When used with RNRSERVICE\_REGISTER, the *lpszComment* field of the network defined in *lpqsRegInfo* is checked for validity and stored persistently.</span></span> <span data-ttu-id="9376a-119">При использовании с РНРСЕРВИЦЕ \_ DELETE и определенная сеть имеет понятное имя, понятное имя удаляется, но сетевая запись остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="9376a-119">When used with RNRSERVICE\_DELETE and the defined network has a friendly name, the friendly name is removed but the network entry is left intact.</span></span>

</dd> <dt>

<span data-ttu-id="9376a-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_сеть ALLUSERS (NLA) \_</span><span class="sxs-lookup"><span data-stu-id="9376a-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA\_ALLUSERS\_NETWORK</span></span>
</dt> <dd>

<span data-ttu-id="9376a-121">При использовании с РНРСЕРВИЦЕ \_ Register запись хранится в постоянном расположении на \_ локальном \_ компьютере hKey, делая ее доступной во время запросов для всех пользователей на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9376a-121">When used with RNRSERVICE\_REGISTER, the entry is stored persistently under HKEY\_LOCAL\_MACHINE, making it available during queries to all users on the local computer.</span></span> <span data-ttu-id="9376a-122">При использовании с РНРСЕРВИЦЕ \_ delete указанная сеть удаляется из \_ ЛОКАЛЬНОГО компьютера hKey \_ .</span><span class="sxs-lookup"><span data-stu-id="9376a-122">When used with RNRSERVICE\_DELETE, the specified network is removed from HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="9376a-123">Если указанная сеть отсутствует, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="9376a-123">An error is returned if the specified network is not present.</span></span> <span data-ttu-id="9376a-124">Чтобы удалить сеть из куста реестра текущего пользователя, этот флаг указывать не нужно.</span><span class="sxs-lookup"><span data-stu-id="9376a-124">In order to delete a network from the registry hive of the current user, this flag must not be specified.</span></span> <span data-ttu-id="9376a-125">Этот флаг действителен только в контексте безопасности локального системного администратора.</span><span class="sxs-lookup"><span data-stu-id="9376a-125">This flag is only valid in the security context of a local system administrator.</span></span>

</dd> </dl>

<span data-ttu-id="9376a-126">NLA поддерживает следующие коды ошибок для вызовов функций [**всасетсервице**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="9376a-126">NLA supports the following error codes for [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function calls:</span></span>

| <span data-ttu-id="9376a-127">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9376a-127">Error</span></span>             | <span data-ttu-id="9376a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="9376a-128">Meaning</span></span>                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9376a-129">WSANOTINITIALISED</span><span class="sxs-lookup"><span data-stu-id="9376a-129">WSANOTINITIALISED</span></span> | <span data-ttu-id="9376a-130">Успешный вызов функции [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) для инициализации NLA не выполнялся.</span><span class="sxs-lookup"><span data-stu-id="9376a-130">A successful call to the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function to initialize NLA was not performed.</span></span>                                                                  |
| <span data-ttu-id="9376a-131">всаеакцесс</span><span class="sxs-lookup"><span data-stu-id="9376a-131">WSAEACCESS</span></span>        | <span data-ttu-id="9376a-132">\_Сеть NLA ALLUSERS \_ была указана в *двконтролфлагс* , а не в контексте безопасности локального системного администратора.</span><span class="sxs-lookup"><span data-stu-id="9376a-132">NLA\_ALLUSERS\_NETWORK was specified in *dwControlFlags* while not in the security context of a local system administrator.</span></span>                                                |
| <span data-ttu-id="9376a-133">всаеалреади</span><span class="sxs-lookup"><span data-stu-id="9376a-133">WSAEALREADY</span></span>       | <span data-ttu-id="9376a-134">Указанная сеть уже сохранена запрошенным образом, и в *двконтролфлагс* не указаны флаги для указания обновления существующей записи.</span><span class="sxs-lookup"><span data-stu-id="9376a-134">The specified network is already persistently stored in the requested manner, and no flags were specified in *dwControlFlags* to indicate an update to the existing entry.</span></span> |
| <span data-ttu-id="9376a-135">WSAEAFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="9376a-135">WSAEAFNOSUPPORT</span></span>   | <span data-ttu-id="9376a-136">Указано семейство протоколов, для которого не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9376a-136">A protocol family was specified for which there is no support.</span></span> <span data-ttu-id="9376a-137">В NLA поддерживаются только семейства IP-протоколов.</span><span class="sxs-lookup"><span data-stu-id="9376a-137">Only IP protocol families are supported in NLA.</span></span>                                                             |
| <span data-ttu-id="9376a-138">всаепфносуппорт</span><span class="sxs-lookup"><span data-stu-id="9376a-138">WSAEPFNOSUPPORT</span></span>   | <span data-ttu-id="9376a-139">Был указан протокол, для которого не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9376a-139">A protocol was specified for which there is no support.</span></span> <span data-ttu-id="9376a-140">В NLA поддерживается только протокол IP.</span><span class="sxs-lookup"><span data-stu-id="9376a-140">Only IP protocol is supported in NLA.</span></span>                                                                              |



 

 

 



