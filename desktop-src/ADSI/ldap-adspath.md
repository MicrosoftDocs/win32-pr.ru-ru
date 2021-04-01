---
title: Путь LDAP
description: В этом разделе показан синтаксис, который следует использовать для LDAP ADsPath.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- Путь LDAP
- ADsPath, LDAP, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793879"
---
# <a name="ldap-adspath"></a><span data-ttu-id="eb8c6-105">Путь LDAP</span><span class="sxs-lookup"><span data-stu-id="eb8c6-105">LDAP ADsPath</span></span>

<span data-ttu-id="eb8c6-106">Для поставщика Microsoft LDAP ADsPath необходимо указать следующий формат.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-106">The Microsoft LDAP provider ADsPath requires the following format.</span></span>


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> <span data-ttu-id="eb8c6-107">Левая и правая квадратные скобки ( \[ \] ) обозначают необязательные параметры; она не является литеральной частью строки привязки.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-107">The left and right bracket characters (\[ \]) indicate optional parameters; it is not a literal part of the binding string.</span></span>

 

<span data-ttu-id="eb8c6-108">Имя узла может быть именем компьютера, IP-адресом или доменным именем.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-108">The "HostName" can be a computer name, an IP address, or a domain name.</span></span> <span data-ttu-id="eb8c6-109">Имя сервера также может быть указано в строке привязки.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-109">A server name can also be specified in the binding string.</span></span> <span data-ttu-id="eb8c6-110">Большинство поставщиков LDAP следуют модели, для которой требуется указать имя сервера.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-110">Most LDAP providers follow a model that requires a server name to be specified.</span></span>

<span data-ttu-id="eb8c6-111">"Номер_порта" указывает порт, используемый для соединения.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-111">The "PortNumber" specifies the port to be used for the connection.</span></span> <span data-ttu-id="eb8c6-112">Если номер порта не указан, поставщик LDAP использует номер порта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-112">If no port number is specified, the LDAP provider uses the default port number.</span></span> <span data-ttu-id="eb8c6-113">Номер порта по умолчанию — 389, если не используется SSL-соединение или 636 при использовании SSL-соединения.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-113">The default port number is 389 if not using an SSL connection or 636 if using an SSL connection.</span></span>

<span data-ttu-id="eb8c6-114">"DistinguishedName" указывает различающееся имя конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-114">The "DistinguishedName" specifies the distinguished name of a specific object.</span></span> <span data-ttu-id="eb8c6-115">Различающееся имя для данного объекта гарантированно уникально.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-115">A distinguished name for a given object is guaranteed to be unique.</span></span>

<span data-ttu-id="eb8c6-116">В следующей таблице приведены примеры строк привязки.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-116">The following table lists examples of binding strings.</span></span>



| <span data-ttu-id="eb8c6-117">Пример LDAP ADsPath</span><span class="sxs-lookup"><span data-stu-id="eb8c6-117">LDAP ADsPath example</span></span>                                      | <span data-ttu-id="eb8c6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="eb8c6-118">Description</span></span>                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="eb8c6-119">LDAP</span><span class="sxs-lookup"><span data-stu-id="eb8c6-119">LDAP:</span></span>                                                     | <span data-ttu-id="eb8c6-120">Выполните привязку к корню пространства имен LDAP.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-120">Bind to the root of the LDAP namespace.</span></span>                    |
| <span data-ttu-id="eb8c6-121">LDAP://server01</span><span class="sxs-lookup"><span data-stu-id="eb8c6-121">LDAP://server01</span></span>                                           | <span data-ttu-id="eb8c6-122">Привязка к определенному серверу.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-122">Bind to a specific server.</span></span>                                 |
| <span data-ttu-id="eb8c6-123">LDAP://server01:390</span><span class="sxs-lookup"><span data-stu-id="eb8c6-123">LDAP://server01:390</span></span>                                       | <span data-ttu-id="eb8c6-124">Привязка к определенному серверу по указанному номеру порта.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-124">Bind to a specific server using the specified port number.</span></span> |
| <span data-ttu-id="eb8c6-125">LDAP://кН = Джефф Иванов, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="eb8c6-125">LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span>          | <span data-ttu-id="eb8c6-126">Привязка к определенному объекту.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-126">Bind to a specific object.</span></span>                                 |
| <span data-ttu-id="eb8c6-127">LDAP://server01/CN=Jeff Смит, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="eb8c6-127">LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span> | <span data-ttu-id="eb8c6-128">Привязка к определенному объекту через указанный сервер.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-128">Bind to a specific object through a specific server.</span></span>       |



 

<span data-ttu-id="eb8c6-129">Если для успешного завершения конкретного запроса к каталогу требуется проверка подлинности Kerberos, то строка привязки должна использовать либо независимый от сервера путь, например LDAP://кН = Джефф Smith, CN = Users, DC = Fabrikam, DC = com, либо путь ADsPath с полным именем DNS-сервера, например LDAP://server01.fabrikam.com/CN=Jeff Смит, CN = Users, DC = Fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-129">If Kerberos authentication is required for the successful completion of a specific directory request, the binding string must use either a serverless ADsPath, such as LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, or it must use an ADsPath with a fully qualified DNS server name, such as LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com.</span></span> <span data-ttu-id="eb8c6-130">При привязке к серверу с использованием неструктурированного имени NETBIOS или короткого DNS-имени, например при использовании имени Server01 вместо server01.fabrikam.com, не гарантируется проверка подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-130">Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the name server01 instead of server01.fabrikam.com, is not guaranteed to yield Kerberos authentication.</span></span>

<span data-ttu-id="eb8c6-131">Дополнительные сведения и примеры строк привязки LDAP, а также описание специальных символов, которые можно использовать в строках привязки LDAP, см. в разделе LDAP ADsPath.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-131">For more information and examples of LDAP binding strings, as well as a description of special characters that can be used in LDAP binding strings, see LDAP ADsPath.</span></span>

<span data-ttu-id="eb8c6-132">**Windows 2000 с пакетом обновления 1 (SP1) и выше:** При использовании поставщика LDAP, если строка привязки содержит имя сервера, можно повысить производительность с помощью флага **\_ \_ привязки сервера ADS** с функцией [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или методом [**иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="eb8c6-132">**Windows 2000 with SP1 and later:** With the LDAP provider, if a binding string includes a server name, you can increase performance by using the **ADS\_SERVER\_BIND** flag with the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span> <span data-ttu-id="eb8c6-133">Флаг **\_ \_ привязки сервера ADS** указывает, что указано имя сервера, которое позволяет интерфейсу ADSI избежать дополнительного, ненужного сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-133">The **ADS\_SERVER\_BIND** flag indicates that a server name was specified, which enables ADSI to avoid additional, unnecessary network traffic.</span></span>

## <a name="ldap-special-characters"></a><span data-ttu-id="eb8c6-134">Специальные символы LDAP</span><span class="sxs-lookup"><span data-stu-id="eb8c6-134">LDAP Special Characters</span></span>

<span data-ttu-id="eb8c6-135">В LDAP есть несколько специальных символов, зарезервированных для использования API LDAP.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-135">LDAP has several special characters which are reserved for use by the LDAP API.</span></span> <span data-ttu-id="eb8c6-136">Список специальных символов можно найти в [различающихся именах](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="eb8c6-136">The list of special characters can be found in [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span> <span data-ttu-id="eb8c6-137">Чтобы использовать один из этих символов в параметре ADsPath без создания ошибки, перед символом должен стоять символ обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="eb8c6-137">To use one of these characters in an ADsPath without generating an error, the character must be preceded by a backslash (\\) character.</span></span> <span data-ttu-id="eb8c6-138">Это называется *экранированием* символа.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-138">This is known as *escaping* the character.</span></span> <span data-ttu-id="eb8c6-139">Например, если имя пользователя указано в виде " <last name> , <first name> ", то запятая в значении имени должна быть экранирована.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-139">For example, if a user name is given in the form of "<last name>,<first name>", the comma in the name value must be escaped.</span></span> <span data-ttu-id="eb8c6-140">Результирующая строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb8c6-140">The resulting string would look like this:</span></span>


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="eb8c6-141">Экранированный символ также можно указать с помощью кода шестнадцатеричного символа из двух цифр.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-141">The escaped character can also be specified by its two digit hexadecimal character code.</span></span> <span data-ttu-id="eb8c6-142">Это показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-142">This is shown in the following example.</span></span>


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="eb8c6-143">Непечатаемые символы, такие как перевод строки и возврат каретки, должны быть экранированы и задаваться с помощью кода шестнадцатеричного символа из двух цифр.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-143">Non-printable characters, such as the line feed and carriage return, must be escaped and specified by their two digit hexadecimal character code.</span></span> <span data-ttu-id="eb8c6-144">Это показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="eb8c6-144">This is shown in the following example.</span></span>


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a><span data-ttu-id="eb8c6-145">Дополнительные сведения см. в разделе</span><span class="sxs-lookup"><span data-stu-id="eb8c6-145">For More Information</span></span>

<span data-ttu-id="eb8c6-146">Дополнительные сведения об нотации различающегося имени, используемой службами каталогов, совместимыми с LDAP, см. в разделе [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .</span><span class="sxs-lookup"><span data-stu-id="eb8c6-146">For more information about the distinguished name notation used by LDAP-compliant directory services, see [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt).</span></span>

 

 