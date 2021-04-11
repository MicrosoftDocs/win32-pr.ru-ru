---
description: Метод Жетфилекапабилитиес извлекает список возможностей файла из текущего файла.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'Метод Искардфилеакцесс:: Жетфилекапабилитиес'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265208"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a>Метод Искардфилеакцесс:: Жетфилекапабилитиес

\[Метод **жетфилекапабилитиес** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **жетфилекапабилитиес** извлекает список возможностей файла из текущего файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пппропертиес* \[ в, out\]
</dt> <dd>

Указатель на TLV-структуры (тег, длина, значение). На входе этот параметр указывает файлы, для которых необходимо получить свойства. в выходных данных этот параметр содержит свойства. В следующем примере приведено определение структуры TLV.


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



Дополнительные сведения о структурах TLV см. в разделе [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .

</dd> <dt>

*плпропертиес* \[ в, out\]
</dt> <dd>

Указатель на число TLV записей в *пппропертиес*.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Указывает, следует ли использовать безопасный обмен сообщениями и предварительно выделенные данные.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ Защита \_ обмена сообщениями через SC FL**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**предварительно \_ \_ выделенный SC FL**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Операция успешно завершена.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                    |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Передан неверный указатель.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                        |



 

## <a name="remarks"></a>Комментарии

Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искардфилеакцесс**](iscardfileaccess.md)
</dt> </dl>

 

 
