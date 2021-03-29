---
title: Функция обратного вызова Расадминрелеасеипаддресс
description: Функция Расадминрелеасеипаддресс — это определяемая приложением функция, экспортируемая сторонней библиотекой DLL администрирования сервера удаленного доступа.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- RAS функции обратного вызова Расадминрелеасеипаддресс
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793512"
---
# <a name="rasadminreleaseipaddress-callback-function"></a><span data-ttu-id="d1797-104">Функция обратного вызова Расадминрелеасеипаддресс</span><span class="sxs-lookup"><span data-stu-id="d1797-104">RasAdminReleaseIpAddress callback function</span></span>

<span data-ttu-id="d1797-105">\[Функция **расадминрелеасеипаддресс** доступна для использования в Windows NT 4,0 и недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="d1797-105">\[The **RasAdminReleaseIpAddress** function is available for use in Windows NT 4.0 and is unavailable in subsequent versions.</span></span> <span data-ttu-id="d1797-106">Вместо этого используйте [**мпрадминрелеасеипаддресс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span><span class="sxs-lookup"><span data-stu-id="d1797-106">Instead, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span></span>

<span data-ttu-id="d1797-107">Функция **расадминрелеасеипаддресс** — это определяемая приложением функция, экспортируемая сторонней библиотекой DLL администрирования сервера удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="d1797-107">The **RasAdminReleaseIpAddress** function is an application-defined function that is exported by a third-party RAS server administration DLL.</span></span> <span data-ttu-id="d1797-108">Служба RAS вызывает эту функцию, чтобы уведомить библиотеку DLL о том, что удаленный клиент был отключен и что IP-адрес должен быть освобожден.</span><span class="sxs-lookup"><span data-stu-id="d1797-108">RAS calls this function to notify the DLL that the remote client was disconnected and that the IP address should be released.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1797-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1797-109">Syntax</span></span>


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a><span data-ttu-id="d1797-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1797-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1797-111">*лпсзусернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1797-111">*lpszUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1797-112">Задает указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя удаленного пользователя, для которого IP-адрес был ранее получен с помощью функции [**расадминжетипаддрессфорусер**](rasadmingetipaddressforuser.md) .</span><span class="sxs-lookup"><span data-stu-id="d1797-112">Specifies the pointer to a null-terminated Unicode string that specifies the name of a remote user for whom an IP address was previously obtained using the [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d1797-113">*лпсзпортнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1797-113">*lpszPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1797-114">Указатель на строку в Юникоде, заканчивающуюся нулем, которая указывает имя порта, к которому подключен пользователь, указанный параметром *лпсзусернаме* .</span><span class="sxs-lookup"><span data-stu-id="d1797-114">Pointer to a null-terminated Unicode string that specifies the name of the port on which the user specified by *lpszUserName* is connected.</span></span>

</dd> <dt>

<span data-ttu-id="d1797-115">*пипаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1797-115">*pipAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1797-116">Указатель на переменную **reduce** , которая указывает IP-адрес, возвращенный этим пользователем в предыдущем вызове [**расадминжетипаддрессфорусер**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="d1797-116">Pointer to an **IPADDR** variable that specifies the IP address returned for this user in a previous call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1797-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1797-117">Return value</span></span>

<span data-ttu-id="d1797-118">Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="d1797-118">There is no extended error information for this function; do no call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1797-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1797-119">Remarks</span></span>

<span data-ttu-id="d1797-120">Сервер RAS вызывает функцию **расадминрелеасеипаддресс** , только если приложение вернуло **значение true** в параметре *Бнотифирелеасе* во время предыдущего вызова [**Расадминжетипаддрессфорусер**](rasadmingetipaddressforuser.md) для пользователя, указанного параметром *лпсзусернаме* .</span><span class="sxs-lookup"><span data-stu-id="d1797-120">The RAS server calls the **RasAdminReleaseIpAddress** function only if the application returned **TRUE** in the *bNotifyRelease* parameter during the earlier call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) for the user specified by the *lpszUserName* parameter.</span></span>

<span data-ttu-id="d1797-121">Программа установки для библиотеки DLL администрирования RAS стороннего производителя должна зарегистрировать библиотеку DLL в службе RAS, предоставив сведения в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="d1797-121">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="d1797-122">Чтобы зарегистрировать библиотеку DLL, задайте в этом разделе следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d1797-122">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="d1797-123">Имя значения</span><span class="sxs-lookup"><span data-stu-id="d1797-123">Value name</span></span>    | <span data-ttu-id="d1797-124">Данные</span><span class="sxs-lookup"><span data-stu-id="d1797-124">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d1797-125">*Отображаемое имя*</span><span class="sxs-lookup"><span data-stu-id="d1797-125">*DisplayName*</span></span> | <span data-ttu-id="d1797-126">Строка **reg \_ SZ** , которая содержит ПОНЯТНОЕ имя библиотеки DLL, отображаемое пользователем.</span><span class="sxs-lookup"><span data-stu-id="d1797-126">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="d1797-127">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="d1797-127">*DLLPath*</span></span>     | <span data-ttu-id="d1797-128">Строка **reg \_ SZ** , содержащая полный путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="d1797-128">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="d1797-129">Например, запись реестра для библиотеки DLL администрирования RAS из вымышленной компании с названием «прочисление» может быть:</span><span class="sxs-lookup"><span data-stu-id="d1797-129">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="d1797-130">*DisplayName*: **reg \_ SZ** : в *формате DLL-* библиотеки администрирования RAS: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="d1797-130">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL *DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="d1797-131">Программа установки библиотеки DLL администрирования RAS должна также предоставлять функции удаления и удаления.</span><span class="sxs-lookup"><span data-stu-id="d1797-131">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="d1797-132">Если пользователь удаляет библиотеку DLL, программа установки должна удалить записи реестра библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="d1797-132">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 