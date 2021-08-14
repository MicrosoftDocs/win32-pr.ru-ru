---
title: Функция Дсресторепрепаре (Нтдсбкли. h)
description: Подключается к указанному серверу каталогов и готовит его к операции восстановления.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсресторепрепаре
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11b844919cc459788bbd8acda722a68344ae16807e45be9bd6dcd5780b09d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191810"
---
# <a name="dsrestoreprepare-function"></a>Функция Дсресторепрепаре

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. начиная с Windows Vista используйте вместо этого [служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Функция **дсресторепрепаре** подключается к указанному серверу каталогов и подготавливает ее для операции восстановления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сзсервернаме* \[ окне\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит имя восстанавливаемого сервера. Предыдущие обратные косые черты необязательны. Сервер должен быть тем же компьютером, из которого вызывается эта функция. Имя сервера не может содержать символы подчеркивания ( \_ ). Пример имени сервера — \\ \\ Server1.

</dd> <dt>

*ртфлаг* \[ окне\]
</dt> <dd>

Указывает тип выполняемого восстановления. Это может быть ноль или одно из следующих значений.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**\_CATCHUP типа \_ восстановления**


</dt> <dd>

По умолчанию. Восстановленная версия выверена с помощью стандартной логики сверки, поэтому восстановленный DIT может синхронизироваться с другими компьютерами Enterprise Server.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**\_аусоратативе типа \_ восстановления**


</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**тип восстановления в \_ \_ сети**


</dt> <dd>

Не поддерживается. Восстановление выполняется, когда NTDS находится в сети.

</dd> </dl> </dd> <dt>

*пвекспиритокен* \[ окне\]
</dt> <dd>

Указатель на маркер срока действия, связанный с восстанавливаемой резервной копией. Этот маркер был получен из функции [**дсбаккуппрепаре**](dsbackupprepare.md) при резервном копировании каталога.

Если этот параметр имеет **значение NULL**, то маркер, возвращаемый в *ФБК* , можно использовать только для получения каталогов восстановления с помощью функции [**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md) . Этот обработчик нельзя использовать для других функций восстановления.

</dd> <dt>

*кбекспиритокенсизе* \[ окне\]
</dt> <dd>

Содержит размер (в байтах) токена срока действия в *пвекспиритокен*.

</dd> <dt>

*ФБК* \[ заполняет\]
</dt> <dd>

Указатель на значение **ХБК** , которое получает маркер для восстановления. Этот маркер используется при вызове других функций восстановления службы каталогов, таких как [**дсбаккупопенфиле**](dsbackupopenfile.md) и [**дсресторинд**](dsrestoreend.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвращает стандартные коды **HRESULT** ; в противном случае возвращается код ошибки.

## <a name="remarks"></a>Remarks

Функция **дсресторепрепаре** требует, чтобы вызывающая сторона была членом группы администраторов на сервере.

**Дсресторепрепаре** можно использовать с указанным токеном или без него. Если указан маркер, он проверяется на срок действия, и все операции разрешаются в возвращаемом контексте. Если токен не указан, возвращаемый контекст ограничен и может использоваться только для функции [**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md) . Он не может использоваться для функции [**дсресторерегистер**](dsrestoreregister.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Нтдсбкли. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Нтдсбкли. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Дсресторепрепарев** (Юникод) и **дсресторепрепареа** (ANSI)<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Восстановление сервера Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Функции резервного копирования каталога](directory-backup-functions.md)
</dt> <dt>

[**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**дсресторерегистер**](dsrestoreregister.md)
</dt> <dt>

[**дсресторерегистеркомплете**](dsrestoreregistercomplete.md)
</dt> <dt>

[**дсресторинд**](dsrestoreend.md)
</dt> </dl>

 

