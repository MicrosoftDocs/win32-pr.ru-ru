---
description: Функция Аусзфрицентралакцессполицикаллбакк является определяемой приложением функцией, которая освобождает память, выделенную функцией Аусзжетцентралакцессполицикаллбакк.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Функция обратного вызова Аусзфрицентралакцессполицикаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273098"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>Функция обратного вызова Аусзфрицентралакцессполицикаллбакк

Функция *аусзфрицентралакцессполицикаллбакк* является определяемой приложением функцией, которая освобождает память, выделенную функцией [*аусзжетцентралакцессполицикаллбакк*](authzgetcentralaccesspolicycallback-.md) . *Аусзфрицентралакцессполицикаллбакк* — это заполнитель для имени определяемой приложением функции.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пцентралакцессполици* \[ окне\]
</dt> <dd>

Указатель на политику централизованного доступа, которую необходимо освободить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, функция возвращает **значение true**.

Если функция не может выполнить вычисление, она возвращает **значение false**. Используйте [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , чтобы вернуть ошибку в функцию проверки доступа.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ сведения о инициализации AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*аусзжетцентралакцессполицикаллбакк*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
