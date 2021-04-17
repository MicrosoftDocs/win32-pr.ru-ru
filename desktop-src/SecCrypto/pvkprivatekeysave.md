---
description: Сохраняет закрытый ключ и соответствующий открытый ключ в указанном файле.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: Функция Пвкприватекэйсаве
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683942"
---
# <a name="pvkprivatekeysave-function"></a>Функция Пвкприватекэйсаве

> [!IMPORTANT]
> Это нерекомендуемый API. Корпорация Майкрософт может удалить этот API в будущих выпусках.

 

Функция **пвкприватекэйсаве** сохраняет [*закрытый ключ*](../secgloss/p-gly.md) и соответствующий [*открытый ключ*](../secgloss/p-gly.md) в указанном файле.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хкриптпров* \[ окне\]
</dt> <dd>

Маркер [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).

</dd> <dt>

*hFile* \[ окне\]
</dt> <dd>

Маркер файла, созданного с помощью начального разрешения на чтение и запись и последующее разрешение только на чтение.

</dd> <dt>

*двкэйспек* \[ окне\]
</dt> <dd>

Длинное целое число для типа ключа. Возможные значения: **в \_ Кэйексчанже** или **в \_ сигнатуре**.

</dd> <dt>

*хвндовнер* \[ окне\]
</dt> <dd>

Если для шифрования закрытого ключа требуется пароль, этот параметр является маркером родителя диалогового окна; в противном случае он имеет **значение NULL**.

</dd> <dt>

*пвсзкэйнаме* \[ окне\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, для имени сохраняемого ключа.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Значение **типа DWORD** , указывающее дополнительные параметры для функции. Дополнительные сведения см. в описании параметра *dwFlags* в [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении эта функция возвращает **значение true**. Функция **пвкприватекэйсаве** возвращает **значение false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
