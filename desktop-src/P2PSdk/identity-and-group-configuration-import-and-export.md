---
description: Файлы конфигурации одноранговых узлов и групп можно импортировать и экспортировать из одной конечной точки в другую с помощью функций импорта и экспорта Identity, расположенных в API Identity Manager и группирования.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Импорт и экспорт конфигурации удостоверений и групп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a356f2747e3c8276446568b6f82bcbd773b14af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813825"
---
# <a name="identity-and-group-configuration-import-and-export"></a><span data-ttu-id="0866e-103">Импорт и экспорт конфигурации удостоверений и групп</span><span class="sxs-lookup"><span data-stu-id="0866e-103">Identity and Group Configuration Import and Export</span></span>

<span data-ttu-id="0866e-104">Файлы конфигурации одноранговых узлов и групп можно импортировать и экспортировать из одной конечной точки в другую с помощью функций импорта и экспорта Identity, расположенных в API Identity Manager и группирования.</span><span class="sxs-lookup"><span data-stu-id="0866e-104">Peer identity and group configuration files can be imported and exported from one endpoint to another by using the identity import and export functions located in the Identity Manager and Grouping APIs.</span></span> <span data-ttu-id="0866e-105">Эти функции полезны, так как позволяют пользователю быстро и удобно экспортировать удостоверения и сведения о конфигурации группы с одного компьютера на другой.</span><span class="sxs-lookup"><span data-stu-id="0866e-105">These functions are useful because they allow a user to quickly and conveniently export identities and group configuration information from one computer to another computer.</span></span>

## <a name="importing-and-exporting-peer-identity-data"></a><span data-ttu-id="0866e-106">Импорт и экспорт данных удостоверений однорангового узла</span><span class="sxs-lookup"><span data-stu-id="0866e-106">Importing and Exporting Peer Identity Data</span></span>

<span data-ttu-id="0866e-107">Данные идентификации однорангового узла экспортируются путем вызова [**пиридентитекспорт**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) с именем удостоверения для экспорта и пароля, используемого для шифрования связанных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0866e-107">The identity data of a peer is exported by calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) with the identity name to export and a password used to encrypt the associated credentials.</span></span> <span data-ttu-id="0866e-108">Эта функция возвращает XML-строку, содержащую имя удостоверения однорангового узла, и зашифрованные учетные данные для этого конкретного удостоверения, которые затем можно передать на другой компьютер с помощью внешнего механизма передачи, такого как электронная почта.</span><span class="sxs-lookup"><span data-stu-id="0866e-108">This function returns an XML string that contains the identity name of the peer and the encrypted credentials for that specific identity, which can then be passed to a different computer by using an external transfer mechanism, such as e-mail.</span></span> <span data-ttu-id="0866e-109">В следующем примере показан формат XML-строки:</span><span class="sxs-lookup"><span data-stu-id="0866e-109">The following example shows you the format of the XML string:</span></span>

``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```

<span data-ttu-id="0866e-110">Экспортированные данные удостоверений можно получить путем вызова [**пиридентитимпорт**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)и передачи строки XML с паролем, предоставленным в предыдущем вызове функции [**пиридентитекспорт**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span><span class="sxs-lookup"><span data-stu-id="0866e-110">The exported identity data can be retrieved by calling [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport), and passing in the XML string with the password supplied in the previous call to [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span></span> <span data-ttu-id="0866e-111">Эта функция возвращает имя однорангового узла импортированного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="0866e-111">This function returns the peer name of the imported identity.</span></span> <span data-ttu-id="0866e-112">Импортированное имя удостоверения и учетные данные можно использовать так же, как имя удостоверения, возвращаемое [**пиренумидентитиес**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) или [**пиридентитикреате**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="0866e-112">The imported identity name and credentials can be used just like an identity name returned by [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) or [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span>

> [!Note]  
> <span data-ttu-id="0866e-113">При вызове [**пиридентитекспорт**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)приложение или пользователь API должен предоставить надежный пароль достаточной длины.</span><span class="sxs-lookup"><span data-stu-id="0866e-113">When calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), the application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="0866e-114">Это важно, так как импортированные данные удостоверения содержат закрытый ключ для удостоверения.</span><span class="sxs-lookup"><span data-stu-id="0866e-114">This is important because the imported identity data contains the private key for the identity.</span></span>

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a><span data-ttu-id="0866e-115">Импорт и экспорт конфигурации удостоверения группы</span><span class="sxs-lookup"><span data-stu-id="0866e-115">Importing and Exporting a Group Identity Configuration</span></span>

<span data-ttu-id="0866e-116">Одноранговая группировка позволяет одноранговому узлу экспортировать данные конфигурации группы из одной конечной точки в другую с помощью конкретных API импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="0866e-116">Peer Grouping allows a peer to export group configuration data from one endpoint to another by using specific import and export APIs.</span></span> <span data-ttu-id="0866e-117">Для импорта данных конфигурации идентификатор однорангового узла, выполняющего импорт (и ранее выполняющий экспорт), должен присутствовать на компьютере, на котором будут импортированы данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0866e-117">To import configuration data, the identity of the peer performing the import (and who previously performed the export) must be present on the computer where the configuration data is to be imported.</span></span> <span data-ttu-id="0866e-118">Это удостоверение можно получить, экспортировав и импортировав его с помощью методов, указанных в предыдущем разделе этой статьи: [Импорт и экспорт данных удостоверений однорангового узла](#importing-and-exporting-peer-identity-data).</span><span class="sxs-lookup"><span data-stu-id="0866e-118">This identity can be obtained by exporting and importing it by the methods specified in the previous section of this topic: [Importing and Exporting Peer Identity Data](#importing-and-exporting-peer-identity-data).</span></span>

<span data-ttu-id="0866e-119">Данные конфигурации группы содержат все сведения об удостоверении, которые необходимо присоединить к группе из новой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="0866e-119">The group configuration data contains all of the information for an identity to join a group from a new endpoint.</span></span> <span data-ttu-id="0866e-120">В частности, данные конфигурации содержат цепочку ГМК, имя однорангового узла, имя облака, область и набор флагов, относящихся к PNRP.</span><span class="sxs-lookup"><span data-stu-id="0866e-120">Specifically, the configuration data contains the GMC chain, group peer name, cloud name, scope, and a set of PNRP specific flags.</span></span> <span data-ttu-id="0866e-121">Для удостоверения, владеющего группой, закрытый ключ для группы включается в сведения о конфигурации группы.</span><span class="sxs-lookup"><span data-stu-id="0866e-121">For an identity that owns a group, a private key for the group is included in the group configuration information.</span></span>

> [!Note]  
> <span data-ttu-id="0866e-122">При вызове [**пирграупекспортконфиг**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)пользователь приложения или API должен предоставить надежный пароль достаточной длины.</span><span class="sxs-lookup"><span data-stu-id="0866e-122">When calling [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), an application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="0866e-123">Это важно, так как импортированные данные удостоверения содержат закрытый ключ для группы.</span><span class="sxs-lookup"><span data-stu-id="0866e-123">This is important because the imported identity data contains the private key for the group.</span></span>

 

<span data-ttu-id="0866e-124">Чтобы экспортировать текущую конфигурацию одноранговой группы, вызовите [**пирграупекспортконфиг**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), передав в нее маркер (полученный предыдущим вызовом [**пирграупжоин**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**пирграупопен**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)или [**пирграупкреате**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) и пароль, используемый для шифрования и защиты файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0866e-124">To export the current peer group configuration, call [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passing in the handle to the group (obtained by a previous call to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen), or [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)), and a password used to encrypt and protect the configuration file.</span></span> <span data-ttu-id="0866e-125">Эта функция возвращает XML-строку, которая содержит конфигурацию в формате следующего примера, который затем можно записать в файл и передать на другой компьютер с помощью внешнего механизма передачи, такого как электронная почта.</span><span class="sxs-lookup"><span data-stu-id="0866e-125">This function returns an XML string that contains the configuration in the format of the following example, which can then be written to a file and passed to another computer by using an external transfer mechanism, such as email.</span></span>

``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

<span data-ttu-id="0866e-126">После получения конфигурации группы в виде XML-строки эту группу можно импортировать, вызвав [**пирграупимпортконфиг**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) с XML-строкой конфигурации и заданным паролем для [**пирграупекспортконфиг**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span><span class="sxs-lookup"><span data-stu-id="0866e-126">After obtaining the group configuration as an XML string, the group can be imported by calling [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) with the configuration XML string and the specific password supplied to [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span></span> <span data-ttu-id="0866e-127">Эта функция возвращает имя удостоверения и имя однорангового узла, которые затем можно передать в [**пирграупопен**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) и соединение с установленной группой.</span><span class="sxs-lookup"><span data-stu-id="0866e-127">This function returns an identity name and a group peer name, which can then be supplied to [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) and a connection to the group established.</span></span>

 

 



