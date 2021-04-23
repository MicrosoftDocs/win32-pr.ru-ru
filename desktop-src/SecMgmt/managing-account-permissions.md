---
description: LSA предоставляет несколько функций, которые могут вызываться приложениями для перечисления или установки привилегий для учетных записей пользователей, групп и локальных групп.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Управление разрешениями учетной записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dc22a4088986abbdaa98d8cdde43415af84905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497193"
---
# <a name="managing-account-permissions"></a><span data-ttu-id="1dfcb-103">Управление разрешениями учетной записи</span><span class="sxs-lookup"><span data-stu-id="1dfcb-103">Managing Account Permissions</span></span>

<span data-ttu-id="1dfcb-104">LSA предоставляет несколько функций, которые могут вызываться приложениями для перечисления или установки [*привилегий*](/windows/desktop/SecGloss/p-gly) для учетных записей пользователей, групп и локальных групп.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-104">The LSA provides several functions that applications can call to enumerate or set [*privileges*](/windows/desktop/SecGloss/p-gly) for user, group, and local group accounts.</span></span>

<span data-ttu-id="1dfcb-105">Прежде чем можно будет управлять сведениями об учетной записи, приложение должно получить обработчик для объекта локальной [**политики**](policy-object.md) , как показано при [открытии обработчика объектов политики](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="1dfcb-105">Before you can manage account information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="1dfcb-106">Кроме того, чтобы перечислить или изменить разрешения для учетной записи, необходимо иметь [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID) для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-106">In addition, to enumerate or edit permissions for an account, you must have the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) for that account.</span></span> <span data-ttu-id="1dfcb-107">Приложение может располагать идентификатор безопасности, используя имя учетной записи, как описано в разделе [Преобразование имен в идентификаторы безопасности и](translating-between-names-and-sids.md)т. д.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-107">Your application can locate a SID given the account name, as described in [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>

<span data-ttu-id="1dfcb-108">Чтобы получить доступ ко всем учетным записям с определенным разрешением, вызовите [**лсаенумератеаккаунтсвисусерригхт**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span><span class="sxs-lookup"><span data-stu-id="1dfcb-108">To access all accounts that have a particular permission, call [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span></span> <span data-ttu-id="1dfcb-109">Эта функция заполняет массив идентификаторами безопасности всех учетных записей, имеющих указанное разрешение.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-109">This function populates an array with the SIDs of all accounts that have the specified permission.</span></span>

<span data-ttu-id="1dfcb-110">После получения идентификатора безопасности учетной записи можно изменить ее разрешения.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-110">After you have obtained the SID of an account, you can modify its permissions.</span></span> <span data-ttu-id="1dfcb-111">Вызовите [**лсааддаккаунтригхтс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) , чтобы добавить разрешения для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-111">Call [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) to add permissions to the account.</span></span> <span data-ttu-id="1dfcb-112">Если указанная учетная запись не существует, **лсааддаккаунтригхтс** ее создает.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-112">If the specified account does not exist, **LsaAddAccountRights** creates it.</span></span> <span data-ttu-id="1dfcb-113">Чтобы удалить разрешения из учетной записи, вызовите [**лсаремовеаккаунтригхтс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span><span class="sxs-lookup"><span data-stu-id="1dfcb-113">To remove permissions from an account, call [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span></span> <span data-ttu-id="1dfcb-114">Если удалить все разрешения из учетной записи, **лсаремовеаккаунтригхтс** также удалит учетную запись.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-114">If you remove all permissions from an account, **LsaRemoveAccountRights** also deletes the account.</span></span>

<span data-ttu-id="1dfcb-115">Приложение может проверить разрешения, назначенные учетной записи в данный момент, вызвав [**лсаенумератеаккаунтригхтс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span><span class="sxs-lookup"><span data-stu-id="1dfcb-115">Your application can check the permissions currently assigned to an account by calling [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span></span> <span data-ttu-id="1dfcb-116">Эта функция заполняет массив [**строковых структур Юникода в \_ формате \_ LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="1dfcb-116">This function populates an array of [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures.</span></span> <span data-ttu-id="1dfcb-117">Каждая структура содержит имя привилегии, удерживаемой указанной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-117">Each structure contains the name of a privilege held by the specified account.</span></span>

<span data-ttu-id="1dfcb-118">В следующем примере к учетной записи добавляется разрешение SeServiceLogonRight.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-118">The following example adds the SeServiceLogonRight permission to an account.</span></span> <span data-ttu-id="1dfcb-119">В этом примере переменная AccountSID указывает идентификатор безопасности учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-119">In this example, the AccountSID variable specifies the SID of the account.</span></span> <span data-ttu-id="1dfcb-120">Дополнительные сведения о поиске SID учетной записи см. в разделе [Преобразование имен и идентификаторов безопасности](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="1dfcb-120">For more information about how to lookup an account SID, see [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



<span data-ttu-id="1dfcb-121">В предыдущем примере функция Инитлсастринг преобразует строку [*Юникода*](/windows/desktop/SecGloss/u-gly) в структуру [**\_ \_ строки Юникода LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="1dfcb-121">In the preceding example, the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="1dfcb-122">Код для этой функции показан в [использовании строк Юникода в формате LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="1dfcb-122">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

 

 
