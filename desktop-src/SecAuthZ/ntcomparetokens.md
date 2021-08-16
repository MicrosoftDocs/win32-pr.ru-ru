---
description: Сравнивает два маркера доступа и определяет, эквивалентны ли они в отношении вызова функции AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Функция Нткомпаретокенс (Нтсеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: a763f6f4238632c3bcc736ebacbd2ff133b1955da673a0397ba9a95ebb87c2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780566"
---
# <a name="ntcomparetokens-function"></a>Функция Нткомпаретокенс

Функция **нткомпаретокенс** сравнивает два [*маркера доступа*](/windows/desktop/SecGloss/a-gly) и определяет, эквивалентны ли они в отношении вызова функции [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фирсттокенхандле* \[ окне\]
</dt> <dd>

Маркер первого маркера доступа для сравнения. Токен должен быть открыт для доступа **к \_ запросам маркеров** .

</dd> <dt>

*Секондтокенхандле* \[ окне\]
</dt> <dd>

Маркер второго маркера доступа для сравнения. Токен должен быть открыт для доступа **к \_ запросам маркеров** .

</dd> <dt>

*Равно* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает значение, указывающее, эквивалентны ли маркеры, представленные параметрами *фирсттокенхандле* и *секондтокенхандле* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, функция возвращает состояние \_ Success.

Если функция завершается ошибкой, возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Remarks

Два маркера управления доступом считаются эквивалентными, если выполняются все перечисленные ниже условия.

-   Каждый [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID), присутствующий в обоих маркерах, также имеется в другом токене.
-   Ни один из маркеров, ни оба не ограничены.
-   Если оба токена ограничены, каждый идентификатор безопасности, ограниченный в одном маркере, также ограничен в другом токене.
-   Все привилегии, имеющиеся в обоих маркерах, также существуют в другом маркере.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Нтсеапи. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

