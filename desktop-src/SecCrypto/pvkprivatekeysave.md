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
ms.openlocfilehash: 3a2eed4b907f7c22414634a4b1ef49df6ca780181109a7396de2f8aa1776b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901213"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
