---
UID: ''
title: Функция Шжетфолдерпасекс
description: Извлекает путь к известной папке, определяемой параметром КНОВНФОЛДЕРИД.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: a071246fadaa971b88e894dff8cb307a38d26b959d8f431972cc4be476344c9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047177"
---
# <a name="shgetfolderpathex-function"></a>Функция Шжетфолдерпасекс

## <a name="description"></a>Описание

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.
Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Получает полный путь к известной папке, идентифицируемой [кновнфолдерид](/windows/desktop/shell/knownfolderid)папки.
Это расширяет [шжеткновнфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , позволяя задавать начальный размер строкового буфера.

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a>Параметры

### <a name="rfid-in"></a>RFID [in]

Ссылка на **кновнфолдерид** , определяющая папку.

### <a name="dwflags-in"></a>dwFlags [in]

Флаги, указывающие специальные параметры извлечения.
Это значение может быть равно 0; в противном случае — одно или несколько значений [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .

### <a name="htoken-in-optional"></a>Хтокен [in, необязательный]

[Маркер доступа](/windows/desktop/SecAuthZ/access-tokens) , представляющий конкретного пользователя.
Если этот параметр имеет **значение NULL**, то есть наиболее распространенный способ использования, функция запрашивает у текущего пользователя доступ к известной папке.

Запросите папку конкретного пользователя, передав *хтокен* этого пользователя.
Обычно это делается в контексте службы, обладающей достаточными привилегиями для получения маркера данного пользователя.
Этот маркер должен быть открыт с правами [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) и [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .
В некоторых случаях также необходимо включить [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).
Кроме передачи *хтокен* пользователя, необходимо подключить куст реестра для конкретного пользователя.
Дополнительные сведения о проблемах, связанных с управлением доступом, см. в статье [Контроль доступа](/windows/desktop/SecAuthZ/access-control) .

При назначении параметра *хтокен* значение-1 указывает на пользователя по умолчанию.
Это позволяет клиентам [шжеткновнфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) находить расположения папок (например, папки **рабочего стола** ) для пользователя по умолчанию.
Профиль пользователя по умолчанию дублируется при создании новой учетной записи пользователя и включает специальные папки, такие как **документы** и **Рабочий стол**.
Все элементы, добавленные в папку пользователя по умолчанию, также отображаются в любой новой учетной записи пользователя.
Обратите внимание, что для доступа к папкам пользователя по умолчанию требуются права администратора.

### <a name="pszpath-out"></a>Псзпас [out]

Строка в Юникоде, заканчивающаяся символом NULL.
Этот буфер должен иметь размер Кчпас.
Когда **шжетфолдерпасекс** возвращается успешно, этот параметр содержит путь к известной папке.

### <a name="cchpath-in"></a>Кчпас [in]

Размер буфера *ппсзпас* в символах.

## <a name="returns"></a>Возвращаемое значение

Возвращает **S_OK** в случае успеха или значение ошибки в противном случае.

## <a name="remarks"></a>Remarks

Так как [шжетфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) является оболочкой для [шжеткновнфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), эта функция (**шжетфолдерпасекс**) также служит расширением для **шжетфолдерпас**.

## <a name="see-also"></a>См. также раздел

[кновнфолдерид](/windows/desktop/shell/knownfolderid)

[KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[шжетфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[шжеткновнфолдеридлист](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[шжеткновнфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
