var Kd = (e) => {
  throw TypeError(e);
};
var Ba = (e, t, n) => t.has(e) || Kd("Cannot " + n);
var A = (e, t, n) => (
    Ba(e, t, "read from private field"), n ? n.call(e) : t.get(e)
  ),
  q = (e, t, n) =>
    t.has(e)
      ? Kd("Cannot add the same private member more than once")
      : t instanceof WeakSet
      ? t.add(e)
      : t.set(e, n),
  $ = (e, t, n, r) => (
    Ba(e, t, "write to private field"), r ? r.call(e, n) : t.set(e, n), n
  ),
  Me = (e, t, n) => (Ba(e, t, "access private method"), n);
var Is = (e, t, n, r) => ({
  set _(i) {
    $(e, t, i, n);
  },
  get _() {
    return A(e, t, r);
  },
});
function e1(e, t) {
  for (var n = 0; n < t.length; n++) {
    const r = t[n];
    if (typeof r != "string" && !Array.isArray(r)) {
      for (const i in r)
        if (i !== "default" && !(i in e)) {
          const s = Object.getOwnPropertyDescriptor(r, i);
          s &&
            Object.defineProperty(
              e,
              i,
              s.get ? s : { enumerable: !0, get: () => r[i] }
            );
        }
    }
  }
  return Object.freeze(
    Object.defineProperty(e, Symbol.toStringTag, { value: "Module" })
  );
}
(function () {
  const t = document.createElement("link").relList;
  if (t && t.supports && t.supports("modulepreload")) return;
  for (const i of document.querySelectorAll('link[rel="modulepreload"]')) r(i);
  new MutationObserver((i) => {
    for (const s of i)
      if (s.type === "childList")
        for (const o of s.addedNodes)
          o.tagName === "LINK" && o.rel === "modulepreload" && r(o);
  }).observe(document, { childList: !0, subtree: !0 });
  function n(i) {
    const s = {};
    return (
      i.integrity && (s.integrity = i.integrity),
      i.referrerPolicy && (s.referrerPolicy = i.referrerPolicy),
      i.crossOrigin === "use-credentials"
        ? (s.credentials = "include")
        : i.crossOrigin === "anonymous"
        ? (s.credentials = "omit")
        : (s.credentials = "same-origin"),
      s
    );
  }
  function r(i) {
    if (i.ep) return;
    i.ep = !0;
    const s = n(i);
    fetch(i.href, s);
  }
})();
function Qp(e) {
  return e && e.__esModule && Object.prototype.hasOwnProperty.call(e, "default")
    ? e.default
    : e;
}
var Gp = { exports: {} },
  sa = {},
  qp = { exports: {} },
  W = {};
/**
 * @license React
 * react.production.min.js
 *
 * Copyright (c) Facebook, Inc. and its affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */ var Ts = Symbol.for("react.element"),
  t1 = Symbol.for("react.portal"),
  n1 = Symbol.for("react.fragment"),
  r1 = Symbol.for("react.strict_mode"),
  i1 = Symbol.for("react.profiler"),
  s1 = Symbol.for("react.provider"),
  o1 = Symbol.for("react.context"),
  a1 = Symbol.for("react.forward_ref"),
  l1 = Symbol.for("react.suspense"),
  u1 = Symbol.for("react.memo"),
  c1 = Symbol.for("react.lazy"),
  Qd = Symbol.iterator;
function d1(e) {
  return e === null || typeof e != "object"
    ? null
    : ((e = (Qd && e[Qd]) || e["@@iterator"]),
      typeof e == "function" ? e : null);
}
var Xp = {
    isMounted: function () {
      return !1;
    },
    enqueueForceUpdate: function () {},
    enqueueReplaceState: function () {},
    enqueueSetState: function () {},
  },
  Yp = Object.assign,
  Zp = {};
function fi(e, t, n) {
  (this.props = e),
    (this.context = t),
    (this.refs = Zp),
    (this.updater = n || Xp);
}
fi.prototype.isReactComponent = {};
fi.prototype.setState = function (e, t) {
  if (typeof e != "object" && typeof e != "function" && e != null)
    throw Error(
      "setState(...): takes an object of state variables to update or a function which returns an object of state variables."
    );
  this.updater.enqueueSetState(this, e, t, "setState");
};
fi.prototype.forceUpdate = function (e) {
  this.updater.enqueueForceUpdate(this, e, "forceUpdate");
};
function Jp() {}
Jp.prototype = fi.prototype;
function Yu(e, t, n) {
  (this.props = e),
    (this.context = t),
    (this.refs = Zp),
    (this.updater = n || Xp);
}
var Zu = (Yu.prototype = new Jp());
Zu.constructor = Yu;
Yp(Zu, fi.prototype);
Zu.isPureReactComponent = !0;
var Gd = Array.isArray,
  em = Object.prototype.hasOwnProperty,
  Ju = { current: null },
  tm = { key: !0, ref: !0, __self: !0, __source: !0 };
function nm(e, t, n) {
  var r,
    i = {},
    s = null,
    o = null;
  if (t != null)
    for (r in (t.ref !== void 0 && (o = t.ref),
    t.key !== void 0 && (s = "" + t.key),
    t))
      em.call(t, r) && !tm.hasOwnProperty(r) && (i[r] = t[r]);
  var a = arguments.length - 2;
  if (a === 1) i.children = n;
  else if (1 < a) {
    for (var l = Array(a), u = 0; u < a; u++) l[u] = arguments[u + 2];
    i.children = l;
  }
  if (e && e.defaultProps)
    for (r in ((a = e.defaultProps), a)) i[r] === void 0 && (i[r] = a[r]);
  return {
    $$typeof: Ts,
    type: e,
    key: s,
    ref: o,
    props: i,
    _owner: Ju.current,
  };
}
function f1(e, t) {
  return {
    $$typeof: Ts,
    type: e.type,
    key: t,
    ref: e.ref,
    props: e.props,
    _owner: e._owner,
  };
}
function ec(e) {
  return typeof e == "object" && e !== null && e.$$typeof === Ts;
}
function h1(e) {
  var t = { "=": "=0", ":": "=2" };
  return (
    "$" +
    e.replace(/[=:]/g, function (n) {
      return t[n];
    })
  );
}
var qd = /\/+/g;
function Ua(e, t) {
  return typeof e == "object" && e !== null && e.key != null
    ? h1("" + e.key)
    : t.toString(36);
}
function oo(e, t, n, r, i) {
  var s = typeof e;
  (s === "undefined" || s === "boolean") && (e = null);
  var o = !1;
  if (e === null) o = !0;
  else
    switch (s) {
      case "string":
      case "number":
        o = !0;
        break;
      case "object":
        switch (e.$$typeof) {
          case Ts:
          case t1:
            o = !0;
        }
    }
  if (o)
    return (
      (o = e),
      (i = i(o)),
      (e = r === "" ? "." + Ua(o, 0) : r),
      Gd(i)
        ? ((n = ""),
          e != null && (n = e.replace(qd, "$&/") + "/"),
          oo(i, t, n, "", function (u) {
            return u;
          }))
        : i != null &&
          (ec(i) &&
            (i = f1(
              i,
              n +
                (!i.key || (o && o.key === i.key)
                  ? ""
                  : ("" + i.key).replace(qd, "$&/") + "/") +
                e
            )),
          t.push(i)),
      1
    );
  if (((o = 0), (r = r === "" ? "." : r + ":"), Gd(e)))
    for (var a = 0; a < e.length; a++) {
      s = e[a];
      var l = r + Ua(s, a);
      o += oo(s, t, n, l, i);
    }
  else if (((l = d1(e)), typeof l == "function"))
    for (e = l.call(e), a = 0; !(s = e.next()).done; )
      (s = s.value), (l = r + Ua(s, a++)), (o += oo(s, t, n, l, i));
  else if (s === "object")
    throw (
      ((t = String(e)),
      Error(
        "Objects are not valid as a React child (found: " +
          (t === "[object Object]"
            ? "object with keys {" + Object.keys(e).join(", ") + "}"
            : t) +
          "). If you meant to render a collection of children, use an array instead."
      ))
    );
  return o;
}
function Fs(e, t, n) {
  if (e == null) return e;
  var r = [],
    i = 0;
  return (
    oo(e, r, "", "", function (s) {
      return t.call(n, s, i++);
    }),
    r
  );
}
function p1(e) {
  if (e._status === -1) {
    var t = e._result;
    (t = t()),
      t.then(
        function (n) {
          (e._status === 0 || e._status === -1) &&
            ((e._status = 1), (e._result = n));
        },
        function (n) {
          (e._status === 0 || e._status === -1) &&
            ((e._status = 2), (e._result = n));
        }
      ),
      e._status === -1 && ((e._status = 0), (e._result = t));
  }
  if (e._status === 1) return e._result.default;
  throw e._result;
}
var We = { current: null },
  ao = { transition: null },
  m1 = {
    ReactCurrentDispatcher: We,
    ReactCurrentBatchConfig: ao,
    ReactCurrentOwner: Ju,
  };
function rm() {
  throw Error("act(...) is not supported in production builds of React.");
}
W.Children = {
  map: Fs,
  forEach: function (e, t, n) {
    Fs(
      e,
      function () {
        t.apply(this, arguments);
      },
      n
    );
  },
  count: function (e) {
    var t = 0;
    return (
      Fs(e, function () {
        t++;
      }),
      t
    );
  },
  toArray: function (e) {
    return (
      Fs(e, function (t) {
        return t;
      }) || []
    );
  },
  only: function (e) {
    if (!ec(e))
      throw Error(
        "React.Children.only expected to receive a single React element child."
      );
    return e;
  },
};
W.Component = fi;
W.Fragment = n1;
W.Profiler = i1;
W.PureComponent = Yu;
W.StrictMode = r1;
W.Suspense = l1;
W.__SECRET_INTERNALS_DO_NOT_USE_OR_YOU_WILL_BE_FIRED = m1;
W.act = rm;
W.cloneElement = function (e, t, n) {
  if (e == null)
    throw Error(
      "React.cloneElement(...): The argument must be a React element, but you passed " +
        e +
        "."
    );
  var r = Yp({}, e.props),
    i = e.key,
    s = e.ref,
    o = e._owner;
  if (t != null) {
    if (
      (t.ref !== void 0 && ((s = t.ref), (o = Ju.current)),
      t.key !== void 0 && (i = "" + t.key),
      e.type && e.type.defaultProps)
    )
      var a = e.type.defaultProps;
    for (l in t)
      em.call(t, l) &&
        !tm.hasOwnProperty(l) &&
        (r[l] = t[l] === void 0 && a !== void 0 ? a[l] : t[l]);
  }
  var l = arguments.length - 2;
  if (l === 1) r.children = n;
  else if (1 < l) {
    a = Array(l);
    for (var u = 0; u < l; u++) a[u] = arguments[u + 2];
    r.children = a;
  }
  return { $$typeof: Ts, type: e.type, key: i, ref: s, props: r, _owner: o };
};
W.createContext = function (e) {
  return (
    (e = {
      $$typeof: o1,
      _currentValue: e,
      _currentValue2: e,
      _threadCount: 0,
      Provider: null,
      Consumer: null,
      _defaultValue: null,
      _globalName: null,
    }),
    (e.Provider = { $$typeof: s1, _context: e }),
    (e.Consumer = e)
  );
};
W.createElement = nm;
W.createFactory = function (e) {
  var t = nm.bind(null, e);
  return (t.type = e), t;
};
W.createRef = function () {
  return { current: null };
};
W.forwardRef = function (e) {
  return { $$typeof: a1, render: e };
};
W.isValidElement = ec;
W.lazy = function (e) {
  return { $$typeof: c1, _payload: { _status: -1, _result: e }, _init: p1 };
};
W.memo = function (e, t) {
  return { $$typeof: u1, type: e, compare: t === void 0 ? null : t };
};
W.startTransition = function (e) {
  var t = ao.transition;
  ao.transition = {};
  try {
    e();
  } finally {
    ao.transition = t;
  }
};
W.unstable_act = rm;
W.useCallback = function (e, t) {
  return We.current.useCallback(e, t);
};
W.useContext = function (e) {
  return We.current.useContext(e);
};
W.useDebugValue = function () {};
W.useDeferredValue = function (e) {
  return We.current.useDeferredValue(e);
};
W.useEffect = function (e, t) {
  return We.current.useEffect(e, t);
};
W.useId = function () {
  return We.current.useId();
};
W.useImperativeHandle = function (e, t, n) {
  return We.current.useImperativeHandle(e, t, n);
};
W.useInsertionEffect = function (e, t) {
  return We.current.useInsertionEffect(e, t);
};
W.useLayoutEffect = function (e, t) {
  return We.current.useLayoutEffect(e, t);
};
W.useMemo = function (e, t) {
  return We.current.useMemo(e, t);
};
W.useReducer = function (e, t, n) {
  return We.current.useReducer(e, t, n);
};
W.useRef = function (e) {
  return We.current.useRef(e);
};
W.useState = function (e) {
  return We.current.useState(e);
};
W.useSyncExternalStore = function (e, t, n) {
  return We.current.useSyncExternalStore(e, t, n);
};
W.useTransition = function () {
  return We.current.useTransition();
};
W.version = "18.3.1";
qp.exports = W;
var w = qp.exports;
const mn = Qp(w),
  g1 = e1({ __proto__: null, default: mn }, [w]);
/**
 * @license React
 * react-jsx-runtime.production.min.js
 *
 * Copyright (c) Facebook, Inc. and its affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */ var y1 = w,
  v1 = Symbol.for("react.element"),
  x1 = Symbol.for("react.fragment"),
  w1 = Object.prototype.hasOwnProperty,
  S1 = y1.__SECRET_INTERNALS_DO_NOT_USE_OR_YOU_WILL_BE_FIRED.ReactCurrentOwner,
  P1 = { key: !0, ref: !0, __self: !0, __source: !0 };
function im(e, t, n) {
  var r,
    i = {},
    s = null,
    o = null;
  n !== void 0 && (s = "" + n),
    t.key !== void 0 && (s = "" + t.key),
    t.ref !== void 0 && (o = t.ref);
  for (r in t) w1.call(t, r) && !P1.hasOwnProperty(r) && (i[r] = t[r]);
  if (e && e.defaultProps)
    for (r in ((t = e.defaultProps), t)) i[r] === void 0 && (i[r] = t[r]);
  return {
    $$typeof: v1,
    type: e,
    key: s,
    ref: o,
    props: i,
    _owner: S1.current,
  };
}
sa.Fragment = x1;
sa.jsx = im;
sa.jsxs = im;
Gp.exports = sa;
var P = Gp.exports,
  sm = { exports: {} },
  st = {},
  om = { exports: {} },
  am = {};
/**
 * @license React
 * scheduler.production.min.js
 *
 * Copyright (c) Facebook, Inc. and its affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */ (function (e) {
  function t(R, L) {
    var F = R.length;
    R.push(L);
    e: for (; 0 < F; ) {
      var z = (F - 1) >>> 1,
        Q = R[z];
      if (0 < i(Q, L)) (R[z] = L), (R[F] = Q), (F = z);
      else break e;
    }
  }
  function n(R) {
    return R.length === 0 ? null : R[0];
  }
  function r(R) {
    if (R.length === 0) return null;
    var L = R[0],
      F = R.pop();
    if (F !== L) {
      R[0] = F;
      e: for (var z = 0, Q = R.length, xe = Q >>> 1; z < xe; ) {
        var ge = 2 * (z + 1) - 1,
          Ut = R[ge],
          Ye = ge + 1,
          Pe = R[Ye];
        if (0 > i(Ut, F))
          Ye < Q && 0 > i(Pe, Ut)
            ? ((R[z] = Pe), (R[Ye] = F), (z = Ye))
            : ((R[z] = Ut), (R[ge] = F), (z = ge));
        else if (Ye < Q && 0 > i(Pe, F)) (R[z] = Pe), (R[Ye] = F), (z = Ye);
        else break e;
      }
    }
    return L;
  }
  function i(R, L) {
    var F = R.sortIndex - L.sortIndex;
    return F !== 0 ? F : R.id - L.id;
  }
  if (typeof performance == "object" && typeof performance.now == "function") {
    var s = performance;
    e.unstable_now = function () {
      return s.now();
    };
  } else {
    var o = Date,
      a = o.now();
    e.unstable_now = function () {
      return o.now() - a;
    };
  }
  var l = [],
    u = [],
    c = 1,
    d = null,
    f = 3,
    v = !1,
    y = !1,
    m = !1,
    x = typeof setTimeout == "function" ? setTimeout : null,
    h = typeof clearTimeout == "function" ? clearTimeout : null,
    p = typeof setImmediate < "u" ? setImmediate : null;
  typeof navigator < "u" &&
    navigator.scheduling !== void 0 &&
    navigator.scheduling.isInputPending !== void 0 &&
    navigator.scheduling.isInputPending.bind(navigator.scheduling);
  function g(R) {
    for (var L = n(u); L !== null; ) {
      if (L.callback === null) r(u);
      else if (L.startTime <= R)
        r(u), (L.sortIndex = L.expirationTime), t(l, L);
      else break;
      L = n(u);
    }
  }
  function S(R) {
    if (((m = !1), g(R), !y))
      if (n(l) !== null) (y = !0), G(C);
      else {
        var L = n(u);
        L !== null && B(S, L.startTime - R);
      }
  }
  function C(R, L) {
    (y = !1), m && ((m = !1), h(E), (E = -1)), (v = !0);
    var F = f;
    try {
      for (
        g(L), d = n(l);
        d !== null && (!(d.expirationTime > L) || (R && !j()));

      ) {
        var z = d.callback;
        if (typeof z == "function") {
          (d.callback = null), (f = d.priorityLevel);
          var Q = z(d.expirationTime <= L);
          (L = e.unstable_now()),
            typeof Q == "function" ? (d.callback = Q) : d === n(l) && r(l),
            g(L);
        } else r(l);
        d = n(l);
      }
      if (d !== null) var xe = !0;
      else {
        var ge = n(u);
        ge !== null && B(S, ge.startTime - L), (xe = !1);
      }
      return xe;
    } finally {
      (d = null), (f = F), (v = !1);
    }
  }
  var k = !1,
    T = null,
    E = -1,
    D = 5,
    N = -1;
  function j() {
    return !(e.unstable_now() - N < D);
  }
  function I() {
    if (T !== null) {
      var R = e.unstable_now();
      N = R;
      var L = !0;
      try {
        L = T(!0, R);
      } finally {
        L ? Z() : ((k = !1), (T = null));
      }
    } else k = !1;
  }
  var Z;
  if (typeof p == "function")
    Z = function () {
      p(I);
    };
  else if (typeof MessageChannel < "u") {
    var b = new MessageChannel(),
      H = b.port2;
    (b.port1.onmessage = I),
      (Z = function () {
        H.postMessage(null);
      });
  } else
    Z = function () {
      x(I, 0);
    };
  function G(R) {
    (T = R), k || ((k = !0), Z());
  }
  function B(R, L) {
    E = x(function () {
      R(e.unstable_now());
    }, L);
  }
  (e.unstable_IdlePriority = 5),
    (e.unstable_ImmediatePriority = 1),
    (e.unstable_LowPriority = 4),
    (e.unstable_NormalPriority = 3),
    (e.unstable_Profiling = null),
    (e.unstable_UserBlockingPriority = 2),
    (e.unstable_cancelCallback = function (R) {
      R.callback = null;
    }),
    (e.unstable_continueExecution = function () {
      y || v || ((y = !0), G(C));
    }),
    (e.unstable_forceFrameRate = function (R) {
      0 > R || 125 < R
        ? console.error(
            "forceFrameRate takes a positive int between 0 and 125, forcing frame rates higher than 125 fps is not supported"
          )
        : (D = 0 < R ? Math.floor(1e3 / R) : 5);
    }),
    (e.unstable_getCurrentPriorityLevel = function () {
      return f;
    }),
    (e.unstable_getFirstCallbackNode = function () {
      return n(l);
    }),
    (e.unstable_next = function (R) {
      switch (f) {
        case 1:
        case 2:
        case 3:
          var L = 3;
          break;
        default:
          L = f;
      }
      var F = f;
      f = L;
      try {
        return R();
      } finally {
        f = F;
      }
    }),
    (e.unstable_pauseExecution = function () {}),
    (e.unstable_requestPaint = function () {}),
    (e.unstable_runWithPriority = function (R, L) {
      switch (R) {
        case 1:
        case 2:
        case 3:
        case 4:
        case 5:
          break;
        default:
          R = 3;
      }
      var F = f;
      f = R;
      try {
        return L();
      } finally {
        f = F;
      }
    }),
    (e.unstable_scheduleCallback = function (R, L, F) {
      var z = e.unstable_now();
      switch (
        (typeof F == "object" && F !== null
          ? ((F = F.delay), (F = typeof F == "number" && 0 < F ? z + F : z))
          : (F = z),
        R)
      ) {
        case 1:
          var Q = -1;
          break;
        case 2:
          Q = 250;
          break;
        case 5:
          Q = 1073741823;
          break;
        case 4:
          Q = 1e4;
          break;
        default:
          Q = 5e3;
      }
      return (
        (Q = F + Q),
        (R = {
          id: c++,
          callback: L,
          priorityLevel: R,
          startTime: F,
          expirationTime: Q,
          sortIndex: -1,
        }),
        F > z
          ? ((R.sortIndex = F),
            t(u, R),
            n(l) === null &&
              R === n(u) &&
              (m ? (h(E), (E = -1)) : (m = !0), B(S, F - z)))
          : ((R.sortIndex = Q), t(l, R), y || v || ((y = !0), G(C))),
        R
      );
    }),
    (e.unstable_shouldYield = j),
    (e.unstable_wrapCallback = function (R) {
      var L = f;
      return function () {
        var F = f;
        f = L;
        try {
          return R.apply(this, arguments);
        } finally {
          f = F;
        }
      };
    });
})(am);
om.exports = am;
var C1 = om.exports;
/**
 * @license React
 * react-dom.production.min.js
 *
 * Copyright (c) Facebook, Inc. and its affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */ var E1 = w,
  rt = C1;
function M(e) {
  for (
    var t = "https://reactjs.org/docs/error-decoder.html?invariant=" + e, n = 1;
    n < arguments.length;
    n++
  )
    t += "&args[]=" + encodeURIComponent(arguments[n]);
  return (
    "Minified React error #" +
    e +
    "; visit " +
    t +
    " for the full message or use the non-minified dev environment for full errors and additional helpful warnings."
  );
}
var lm = new Set(),
  Xi = {};
function vr(e, t) {
  ti(e, t), ti(e + "Capture", t);
}
function ti(e, t) {
  for (Xi[e] = t, e = 0; e < t.length; e++) lm.add(t[e]);
}
var tn = !(
    typeof window > "u" ||
    typeof window.document > "u" ||
    typeof window.document.createElement > "u"
  ),
  Ll = Object.prototype.hasOwnProperty,
  T1 =
    /^[:A-Z_a-z\u00C0-\u00D6\u00D8-\u00F6\u00F8-\u02FF\u0370-\u037D\u037F-\u1FFF\u200C-\u200D\u2070-\u218F\u2C00-\u2FEF\u3001-\uD7FF\uF900-\uFDCF\uFDF0-\uFFFD][:A-Z_a-z\u00C0-\u00D6\u00D8-\u00F6\u00F8-\u02FF\u0370-\u037D\u037F-\u1FFF\u200C-\u200D\u2070-\u218F\u2C00-\u2FEF\u3001-\uD7FF\uF900-\uFDCF\uFDF0-\uFFFD\-.0-9\u00B7\u0300-\u036F\u203F-\u2040]*$/,
  Xd = {},
  Yd = {};
function k1(e) {
  return Ll.call(Yd, e)
    ? !0
    : Ll.call(Xd, e)
    ? !1
    : T1.test(e)
    ? (Yd[e] = !0)
    : ((Xd[e] = !0), !1);
}
function A1(e, t, n, r) {
  if (n !== null && n.type === 0) return !1;
  switch (typeof t) {
    case "function":
    case "symbol":
      return !0;
    case "boolean":
      return r
        ? !1
        : n !== null
        ? !n.acceptsBooleans
        : ((e = e.toLowerCase().slice(0, 5)), e !== "data-" && e !== "aria-");
    default:
      return !1;
  }
}
function R1(e, t, n, r) {
  if (t === null || typeof t > "u" || A1(e, t, n, r)) return !0;
  if (r) return !1;
  if (n !== null)
    switch (n.type) {
      case 3:
        return !t;
      case 4:
        return t === !1;
      case 5:
        return isNaN(t);
      case 6:
        return isNaN(t) || 1 > t;
    }
  return !1;
}
function He(e, t, n, r, i, s, o) {
  (this.acceptsBooleans = t === 2 || t === 3 || t === 4),
    (this.attributeName = r),
    (this.attributeNamespace = i),
    (this.mustUseProperty = n),
    (this.propertyName = e),
    (this.type = t),
    (this.sanitizeURL = s),
    (this.removeEmptyString = o);
}
var Re = {};
"children dangerouslySetInnerHTML defaultValue defaultChecked innerHTML suppressContentEditableWarning suppressHydrationWarning style"
  .split(" ")
  .forEach(function (e) {
    Re[e] = new He(e, 0, !1, e, null, !1, !1);
  });
[
  ["acceptCharset", "accept-charset"],
  ["className", "class"],
  ["htmlFor", "for"],
  ["httpEquiv", "http-equiv"],
].forEach(function (e) {
  var t = e[0];
  Re[t] = new He(t, 1, !1, e[1], null, !1, !1);
});
["contentEditable", "draggable", "spellCheck", "value"].forEach(function (e) {
  Re[e] = new He(e, 2, !1, e.toLowerCase(), null, !1, !1);
});
[
  "autoReverse",
  "externalResourcesRequired",
  "focusable",
  "preserveAlpha",
].forEach(function (e) {
  Re[e] = new He(e, 2, !1, e, null, !1, !1);
});
"allowFullScreen async autoFocus autoPlay controls default defer disabled disablePictureInPicture disableRemotePlayback formNoValidate hidden loop noModule noValidate open playsInline readOnly required reversed scoped seamless itemScope"
  .split(" ")
  .forEach(function (e) {
    Re[e] = new He(e, 3, !1, e.toLowerCase(), null, !1, !1);
  });
["checked", "multiple", "muted", "selected"].forEach(function (e) {
  Re[e] = new He(e, 3, !0, e, null, !1, !1);
});
["capture", "download"].forEach(function (e) {
  Re[e] = new He(e, 4, !1, e, null, !1, !1);
});
["cols", "rows", "size", "span"].forEach(function (e) {
  Re[e] = new He(e, 6, !1, e, null, !1, !1);
});
["rowSpan", "start"].forEach(function (e) {
  Re[e] = new He(e, 5, !1, e.toLowerCase(), null, !1, !1);
});
var tc = /[\-:]([a-z])/g;
function nc(e) {
  return e[1].toUpperCase();
}
"accent-height alignment-baseline arabic-form baseline-shift cap-height clip-path clip-rule color-interpolation color-interpolation-filters color-profile color-rendering dominant-baseline enable-background fill-opacity fill-rule flood-color flood-opacity font-family font-size font-size-adjust font-stretch font-style font-variant font-weight glyph-name glyph-orientation-horizontal glyph-orientation-vertical horiz-adv-x horiz-origin-x image-rendering letter-spacing lighting-color marker-end marker-mid marker-start overline-position overline-thickness paint-order panose-1 pointer-events rendering-intent shape-rendering stop-color stop-opacity strikethrough-position strikethrough-thickness stroke-dasharray stroke-dashoffset stroke-linecap stroke-linejoin stroke-miterlimit stroke-opacity stroke-width text-anchor text-decoration text-rendering underline-position underline-thickness unicode-bidi unicode-range units-per-em v-alphabetic v-hanging v-ideographic v-mathematical vector-effect vert-adv-y vert-origin-x vert-origin-y word-spacing writing-mode xmlns:xlink x-height"
  .split(" ")
  .forEach(function (e) {
    var t = e.replace(tc, nc);
    Re[t] = new He(t, 1, !1, e, null, !1, !1);
  });
"xlink:actuate xlink:arcrole xlink:role xlink:show xlink:title xlink:type"
  .split(" ")
  .forEach(function (e) {
    var t = e.replace(tc, nc);
    Re[t] = new He(t, 1, !1, e, "http://www.w3.org/1999/xlink", !1, !1);
  });
["xml:base", "xml:lang", "xml:space"].forEach(function (e) {
  var t = e.replace(tc, nc);
  Re[t] = new He(t, 1, !1, e, "http://www.w3.org/XML/1998/namespace", !1, !1);
});
["tabIndex", "crossOrigin"].forEach(function (e) {
  Re[e] = new He(e, 1, !1, e.toLowerCase(), null, !1, !1);
});
Re.xlinkHref = new He(
  "xlinkHref",
  1,
  !1,
  "xlink:href",
  "http://www.w3.org/1999/xlink",
  !0,
  !1
);
["src", "href", "action", "formAction"].forEach(function (e) {
  Re[e] = new He(e, 1, !1, e.toLowerCase(), null, !0, !0);
});
function rc(e, t, n, r) {
  var i = Re.hasOwnProperty(t) ? Re[t] : null;
  (i !== null
    ? i.type !== 0
    : r ||
      !(2 < t.length) ||
      (t[0] !== "o" && t[0] !== "O") ||
      (t[1] !== "n" && t[1] !== "N")) &&
    (R1(t, n, i, r) && (n = null),
    r || i === null
      ? k1(t) && (n === null ? e.removeAttribute(t) : e.setAttribute(t, "" + n))
      : i.mustUseProperty
      ? (e[i.propertyName] = n === null ? (i.type === 3 ? !1 : "") : n)
      : ((t = i.attributeName),
        (r = i.attributeNamespace),
        n === null
          ? e.removeAttribute(t)
          : ((i = i.type),
            (n = i === 3 || (i === 4 && n === !0) ? "" : "" + n),
            r ? e.setAttributeNS(r, t, n) : e.setAttribute(t, n))));
}
var ln = E1.__SECRET_INTERNALS_DO_NOT_USE_OR_YOU_WILL_BE_FIRED,
  _s = Symbol.for("react.element"),
  Pr = Symbol.for("react.portal"),
  Cr = Symbol.for("react.fragment"),
  ic = Symbol.for("react.strict_mode"),
  Ol = Symbol.for("react.profiler"),
  um = Symbol.for("react.provider"),
  cm = Symbol.for("react.context"),
  sc = Symbol.for("react.forward_ref"),
  jl = Symbol.for("react.suspense"),
  Il = Symbol.for("react.suspense_list"),
  oc = Symbol.for("react.memo"),
  vn = Symbol.for("react.lazy"),
  dm = Symbol.for("react.offscreen"),
  Zd = Symbol.iterator;
function vi(e) {
  return e === null || typeof e != "object"
    ? null
    : ((e = (Zd && e[Zd]) || e["@@iterator"]),
      typeof e == "function" ? e : null);
}
var ce = Object.assign,
  $a;
function Mi(e) {
  if ($a === void 0)
    try {
      throw Error();
    } catch (n) {
      var t = n.stack.trim().match(/\n( *(at )?)/);
      $a = (t && t[1]) || "";
    }
  return (
    `
  ` +
    $a +
    e
  );
}
var Wa = !1;
function Ha(e, t) {
  if (!e || Wa) return "";
  Wa = !0;
  var n = Error.prepareStackTrace;
  Error.prepareStackTrace = void 0;
  try {
    if (t)
      if (
        ((t = function () {
          throw Error();
        }),
        Object.defineProperty(t.prototype, "props", {
          set: function () {
            throw Error();
          },
        }),
        typeof Reflect == "object" && Reflect.construct)
      ) {
        try {
          Reflect.construct(t, []);
        } catch (u) {
          var r = u;
        }
        Reflect.construct(e, [], t);
      } else {
        try {
          t.call();
        } catch (u) {
          r = u;
        }
        e.call(t.prototype);
      }
    else {
      try {
        throw Error();
      } catch (u) {
        r = u;
      }
      e();
    }
  } catch (u) {
    if (u && r && typeof u.stack == "string") {
      for (
        var i = u.stack.split(`
  `),
          s = r.stack.split(`
  `),
          o = i.length - 1,
          a = s.length - 1;
        1 <= o && 0 <= a && i[o] !== s[a];

      )
        a--;
      for (; 1 <= o && 0 <= a; o--, a--)
        if (i[o] !== s[a]) {
          if (o !== 1 || a !== 1)
            do
              if ((o--, a--, 0 > a || i[o] !== s[a])) {
                var l =
                  `
  ` + i[o].replace(" at new ", " at ");
                return (
                  e.displayName &&
                    l.includes("<anonymous>") &&
                    (l = l.replace("<anonymous>", e.displayName)),
                  l
                );
              }
            while (1 <= o && 0 <= a);
          break;
        }
    }
  } finally {
    (Wa = !1), (Error.prepareStackTrace = n);
  }
  return (e = e ? e.displayName || e.name : "") ? Mi(e) : "";
}
function M1(e) {
  switch (e.tag) {
    case 5:
      return Mi(e.type);
    case 16:
      return Mi("Lazy");
    case 13:
      return Mi("Suspense");
    case 19:
      return Mi("SuspenseList");
    case 0:
    case 2:
    case 15:
      return (e = Ha(e.type, !1)), e;
    case 11:
      return (e = Ha(e.type.render, !1)), e;
    case 1:
      return (e = Ha(e.type, !0)), e;
    default:
      return "";
  }
}
function Fl(e) {
  if (e == null) return null;
  if (typeof e == "function") return e.displayName || e.name || null;
  if (typeof e == "string") return e;
  switch (e) {
    case Cr:
      return "Fragment";
    case Pr:
      return "Portal";
    case Ol:
      return "Profiler";
    case ic:
      return "StrictMode";
    case jl:
      return "Suspense";
    case Il:
      return "SuspenseList";
  }
  if (typeof e == "object")
    switch (e.$$typeof) {
      case cm:
        return (e.displayName || "Context") + ".Consumer";
      case um:
        return (e._context.displayName || "Context") + ".Provider";
      case sc:
        var t = e.render;
        return (
          (e = e.displayName),
          e ||
            ((e = t.displayName || t.name || ""),
            (e = e !== "" ? "ForwardRef(" + e + ")" : "ForwardRef")),
          e
        );
      case oc:
        return (
          (t = e.displayName || null), t !== null ? t : Fl(e.type) || "Memo"
        );
      case vn:
        (t = e._payload), (e = e._init);
        try {
          return Fl(e(t));
        } catch {}
    }
  return null;
}
function D1(e) {
  var t = e.type;
  switch (e.tag) {
    case 24:
      return "Cache";
    case 9:
      return (t.displayName || "Context") + ".Consumer";
    case 10:
      return (t._context.displayName || "Context") + ".Provider";
    case 18:
      return "DehydratedFragment";
    case 11:
      return (
        (e = t.render),
        (e = e.displayName || e.name || ""),
        t.displayName || (e !== "" ? "ForwardRef(" + e + ")" : "ForwardRef")
      );
    case 7:
      return "Fragment";
    case 5:
      return t;
    case 4:
      return "Portal";
    case 3:
      return "Root";
    case 6:
      return "Text";
    case 16:
      return Fl(t);
    case 8:
      return t === ic ? "StrictMode" : "Mode";
    case 22:
      return "Offscreen";
    case 12:
      return "Profiler";
    case 21:
      return "Scope";
    case 13:
      return "Suspense";
    case 19:
      return "SuspenseList";
    case 25:
      return "TracingMarker";
    case 1:
    case 0:
    case 17:
    case 2:
    case 14:
    case 15:
      if (typeof t == "function") return t.displayName || t.name || null;
      if (typeof t == "string") return t;
  }
  return null;
}
function Vn(e) {
  switch (typeof e) {
    case "boolean":
    case "number":
    case "string":
    case "undefined":
      return e;
    case "object":
      return e;
    default:
      return "";
  }
}
function fm(e) {
  var t = e.type;
  return (
    (e = e.nodeName) &&
    e.toLowerCase() === "input" &&
    (t === "checkbox" || t === "radio")
  );
}
function N1(e) {
  var t = fm(e) ? "checked" : "value",
    n = Object.getOwnPropertyDescriptor(e.constructor.prototype, t),
    r = "" + e[t];
  if (
    !e.hasOwnProperty(t) &&
    typeof n < "u" &&
    typeof n.get == "function" &&
    typeof n.set == "function"
  ) {
    var i = n.get,
      s = n.set;
    return (
      Object.defineProperty(e, t, {
        configurable: !0,
        get: function () {
          return i.call(this);
        },
        set: function (o) {
          (r = "" + o), s.call(this, o);
        },
      }),
      Object.defineProperty(e, t, { enumerable: n.enumerable }),
      {
        getValue: function () {
          return r;
        },
        setValue: function (o) {
          r = "" + o;
        },
        stopTracking: function () {
          (e._valueTracker = null), delete e[t];
        },
      }
    );
  }
}
function Vs(e) {
  e._valueTracker || (e._valueTracker = N1(e));
}
function hm(e) {
  if (!e) return !1;
  var t = e._valueTracker;
  if (!t) return !0;
  var n = t.getValue(),
    r = "";
  return (
    e && (r = fm(e) ? (e.checked ? "true" : "false") : e.value),
    (e = r),
    e !== n ? (t.setValue(e), !0) : !1
  );
}
function Eo(e) {
  if (((e = e || (typeof document < "u" ? document : void 0)), typeof e > "u"))
    return null;
  try {
    return e.activeElement || e.body;
  } catch {
    return e.body;
  }
}
function _l(e, t) {
  var n = t.checked;
  return ce({}, t, {
    defaultChecked: void 0,
    defaultValue: void 0,
    value: void 0,
    checked: n ?? e._wrapperState.initialChecked,
  });
}
function Jd(e, t) {
  var n = t.defaultValue == null ? "" : t.defaultValue,
    r = t.checked != null ? t.checked : t.defaultChecked;
  (n = Vn(t.value != null ? t.value : n)),
    (e._wrapperState = {
      initialChecked: r,
      initialValue: n,
      controlled:
        t.type === "checkbox" || t.type === "radio"
          ? t.checked != null
          : t.value != null,
    });
}
function pm(e, t) {
  (t = t.checked), t != null && rc(e, "checked", t, !1);
}
function Vl(e, t) {
  pm(e, t);
  var n = Vn(t.value),
    r = t.type;
  if (n != null)
    r === "number"
      ? ((n === 0 && e.value === "") || e.value != n) && (e.value = "" + n)
      : e.value !== "" + n && (e.value = "" + n);
  else if (r === "submit" || r === "reset") {
    e.removeAttribute("value");
    return;
  }
  t.hasOwnProperty("value")
    ? zl(e, t.type, n)
    : t.hasOwnProperty("defaultValue") && zl(e, t.type, Vn(t.defaultValue)),
    t.checked == null &&
      t.defaultChecked != null &&
      (e.defaultChecked = !!t.defaultChecked);
}
function ef(e, t, n) {
  if (t.hasOwnProperty("value") || t.hasOwnProperty("defaultValue")) {
    var r = t.type;
    if (
      !(
        (r !== "submit" && r !== "reset") ||
        (t.value !== void 0 && t.value !== null)
      )
    )
      return;
    (t = "" + e._wrapperState.initialValue),
      n || t === e.value || (e.value = t),
      (e.defaultValue = t);
  }
  (n = e.name),
    n !== "" && (e.name = ""),
    (e.defaultChecked = !!e._wrapperState.initialChecked),
    n !== "" && (e.name = n);
}
function zl(e, t, n) {
  (t !== "number" || Eo(e.ownerDocument) !== e) &&
    (n == null
      ? (e.defaultValue = "" + e._wrapperState.initialValue)
      : e.defaultValue !== "" + n && (e.defaultValue = "" + n));
}
var Di = Array.isArray;
function Vr(e, t, n, r) {
  if (((e = e.options), t)) {
    t = {};
    for (var i = 0; i < n.length; i++) t["$" + n[i]] = !0;
    for (n = 0; n < e.length; n++)
      (i = t.hasOwnProperty("$" + e[n].value)),
        e[n].selected !== i && (e[n].selected = i),
        i && r && (e[n].defaultSelected = !0);
  } else {
    for (n = "" + Vn(n), t = null, i = 0; i < e.length; i++) {
      if (e[i].value === n) {
        (e[i].selected = !0), r && (e[i].defaultSelected = !0);
        return;
      }
      t !== null || e[i].disabled || (t = e[i]);
    }
    t !== null && (t.selected = !0);
  }
}
function Bl(e, t) {
  if (t.dangerouslySetInnerHTML != null) throw Error(M(91));
  return ce({}, t, {
    value: void 0,
    defaultValue: void 0,
    children: "" + e._wrapperState.initialValue,
  });
}
function tf(e, t) {
  var n = t.value;
  if (n == null) {
    if (((n = t.children), (t = t.defaultValue), n != null)) {
      if (t != null) throw Error(M(92));
      if (Di(n)) {
        if (1 < n.length) throw Error(M(93));
        n = n[0];
      }
      t = n;
    }
    t == null && (t = ""), (n = t);
  }
  e._wrapperState = { initialValue: Vn(n) };
}
function mm(e, t) {
  var n = Vn(t.value),
    r = Vn(t.defaultValue);
  n != null &&
    ((n = "" + n),
    n !== e.value && (e.value = n),
    t.defaultValue == null && e.defaultValue !== n && (e.defaultValue = n)),
    r != null && (e.defaultValue = "" + r);
}
function nf(e) {
  var t = e.textContent;
  t === e._wrapperState.initialValue && t !== "" && t !== null && (e.value = t);
}
function gm(e) {
  switch (e) {
    case "svg":
      return "http://www.w3.org/2000/svg";
    case "math":
      return "http://www.w3.org/1998/Math/MathML";
    default:
      return "http://www.w3.org/1999/xhtml";
  }
}
function Ul(e, t) {
  return e == null || e === "http://www.w3.org/1999/xhtml"
    ? gm(t)
    : e === "http://www.w3.org/2000/svg" && t === "foreignObject"
    ? "http://www.w3.org/1999/xhtml"
    : e;
}
var zs,
  ym = (function (e) {
    return typeof MSApp < "u" && MSApp.execUnsafeLocalFunction
      ? function (t, n, r, i) {
          MSApp.execUnsafeLocalFunction(function () {
            return e(t, n, r, i);
          });
        }
      : e;
  })(function (e, t) {
    if (e.namespaceURI !== "http://www.w3.org/2000/svg" || "innerHTML" in e)
      e.innerHTML = t;
    else {
      for (
        zs = zs || document.createElement("div"),
          zs.innerHTML = "<svg>" + t.valueOf().toString() + "</svg>",
          t = zs.firstChild;
        e.firstChild;

      )
        e.removeChild(e.firstChild);
      for (; t.firstChild; ) e.appendChild(t.firstChild);
    }
  });
function Yi(e, t) {
  if (t) {
    var n = e.firstChild;
    if (n && n === e.lastChild && n.nodeType === 3) {
      n.nodeValue = t;
      return;
    }
  }
  e.textContent = t;
}
var Ii = {
    animationIterationCount: !0,
    aspectRatio: !0,
    borderImageOutset: !0,
    borderImageSlice: !0,
    borderImageWidth: !0,
    boxFlex: !0,
    boxFlexGroup: !0,
    boxOrdinalGroup: !0,
    columnCount: !0,
    columns: !0,
    flex: !0,
    flexGrow: !0,
    flexPositive: !0,
    flexShrink: !0,
    flexNegative: !0,
    flexOrder: !0,
    gridArea: !0,
    gridRow: !0,
    gridRowEnd: !0,
    gridRowSpan: !0,
    gridRowStart: !0,
    gridColumn: !0,
    gridColumnEnd: !0,
    gridColumnSpan: !0,
    gridColumnStart: !0,
    fontWeight: !0,
    lineClamp: !0,
    lineHeight: !0,
    opacity: !0,
    order: !0,
    orphans: !0,
    tabSize: !0,
    widows: !0,
    zIndex: !0,
    zoom: !0,
    fillOpacity: !0,
    floodOpacity: !0,
    stopOpacity: !0,
    strokeDasharray: !0,
    strokeDashoffset: !0,
    strokeMiterlimit: !0,
    strokeOpacity: !0,
    strokeWidth: !0,
  },
  b1 = ["Webkit", "ms", "Moz", "O"];
Object.keys(Ii).forEach(function (e) {
  b1.forEach(function (t) {
    (t = t + e.charAt(0).toUpperCase() + e.substring(1)), (Ii[t] = Ii[e]);
  });
});
function vm(e, t, n) {
  return t == null || typeof t == "boolean" || t === ""
    ? ""
    : n || typeof t != "number" || t === 0 || (Ii.hasOwnProperty(e) && Ii[e])
    ? ("" + t).trim()
    : t + "px";
}
function xm(e, t) {
  e = e.style;
  for (var n in t)
    if (t.hasOwnProperty(n)) {
      var r = n.indexOf("--") === 0,
        i = vm(n, t[n], r);
      n === "float" && (n = "cssFloat"), r ? e.setProperty(n, i) : (e[n] = i);
    }
}
var L1 = ce(
  { menuitem: !0 },
  {
    area: !0,
    base: !0,
    br: !0,
    col: !0,
    embed: !0,
    hr: !0,
    img: !0,
    input: !0,
    keygen: !0,
    link: !0,
    meta: !0,
    param: !0,
    source: !0,
    track: !0,
    wbr: !0,
  }
);
function $l(e, t) {
  if (t) {
    if (L1[e] && (t.children != null || t.dangerouslySetInnerHTML != null))
      throw Error(M(137, e));
    if (t.dangerouslySetInnerHTML != null) {
      if (t.children != null) throw Error(M(60));
      if (
        typeof t.dangerouslySetInnerHTML != "object" ||
        !("__html" in t.dangerouslySetInnerHTML)
      )
        throw Error(M(61));
    }
    if (t.style != null && typeof t.style != "object") throw Error(M(62));
  }
}
function Wl(e, t) {
  if (e.indexOf("-") === -1) return typeof t.is == "string";
  switch (e) {
    case "annotation-xml":
    case "color-profile":
    case "font-face":
    case "font-face-src":
    case "font-face-uri":
    case "font-face-format":
    case "font-face-name":
    case "missing-glyph":
      return !1;
    default:
      return !0;
  }
}
var Hl = null;
function ac(e) {
  return (
    (e = e.target || e.srcElement || window),
    e.correspondingUseElement && (e = e.correspondingUseElement),
    e.nodeType === 3 ? e.parentNode : e
  );
}
var Kl = null,
  zr = null,
  Br = null;
function rf(e) {
  if ((e = Rs(e))) {
    if (typeof Kl != "function") throw Error(M(280));
    var t = e.stateNode;
    t && ((t = ca(t)), Kl(e.stateNode, e.type, t));
  }
}
function wm(e) {
  zr ? (Br ? Br.push(e) : (Br = [e])) : (zr = e);
}
function Sm() {
  if (zr) {
    var e = zr,
      t = Br;
    if (((Br = zr = null), rf(e), t)) for (e = 0; e < t.length; e++) rf(t[e]);
  }
}
function Pm(e, t) {
  return e(t);
}
function Cm() {}
var Ka = !1;
function Em(e, t, n) {
  if (Ka) return e(t, n);
  Ka = !0;
  try {
    return Pm(e, t, n);
  } finally {
    (Ka = !1), (zr !== null || Br !== null) && (Cm(), Sm());
  }
}
function Zi(e, t) {
  var n = e.stateNode;
  if (n === null) return null;
  var r = ca(n);
  if (r === null) return null;
  n = r[t];
  e: switch (t) {
    case "onClick":
    case "onClickCapture":
    case "onDoubleClick":
    case "onDoubleClickCapture":
    case "onMouseDown":
    case "onMouseDownCapture":
    case "onMouseMove":
    case "onMouseMoveCapture":
    case "onMouseUp":
    case "onMouseUpCapture":
    case "onMouseEnter":
      (r = !r.disabled) ||
        ((e = e.type),
        (r = !(
          e === "button" ||
          e === "input" ||
          e === "select" ||
          e === "textarea"
        ))),
        (e = !r);
      break e;
    default:
      e = !1;
  }
  if (e) return null;
  if (n && typeof n != "function") throw Error(M(231, t, typeof n));
  return n;
}
var Ql = !1;
if (tn)
  try {
    var xi = {};
    Object.defineProperty(xi, "passive", {
      get: function () {
        Ql = !0;
      },
    }),
      window.addEventListener("test", xi, xi),
      window.removeEventListener("test", xi, xi);
  } catch {
    Ql = !1;
  }
function O1(e, t, n, r, i, s, o, a, l) {
  var u = Array.prototype.slice.call(arguments, 3);
  try {
    t.apply(n, u);
  } catch (c) {
    this.onError(c);
  }
}
var Fi = !1,
  To = null,
  ko = !1,
  Gl = null,
  j1 = {
    onError: function (e) {
      (Fi = !0), (To = e);
    },
  };
function I1(e, t, n, r, i, s, o, a, l) {
  (Fi = !1), (To = null), O1.apply(j1, arguments);
}
function F1(e, t, n, r, i, s, o, a, l) {
  if ((I1.apply(this, arguments), Fi)) {
    if (Fi) {
      var u = To;
      (Fi = !1), (To = null);
    } else throw Error(M(198));
    ko || ((ko = !0), (Gl = u));
  }
}
function xr(e) {
  var t = e,
    n = e;
  if (e.alternate) for (; t.return; ) t = t.return;
  else {
    e = t;
    do (t = e), t.flags & 4098 && (n = t.return), (e = t.return);
    while (e);
  }
  return t.tag === 3 ? n : null;
}
function Tm(e) {
  if (e.tag === 13) {
    var t = e.memoizedState;
    if (
      (t === null && ((e = e.alternate), e !== null && (t = e.memoizedState)),
      t !== null)
    )
      return t.dehydrated;
  }
  return null;
}
function sf(e) {
  if (xr(e) !== e) throw Error(M(188));
}
function _1(e) {
  var t = e.alternate;
  if (!t) {
    if (((t = xr(e)), t === null)) throw Error(M(188));
    return t !== e ? null : e;
  }
  for (var n = e, r = t; ; ) {
    var i = n.return;
    if (i === null) break;
    var s = i.alternate;
    if (s === null) {
      if (((r = i.return), r !== null)) {
        n = r;
        continue;
      }
      break;
    }
    if (i.child === s.child) {
      for (s = i.child; s; ) {
        if (s === n) return sf(i), e;
        if (s === r) return sf(i), t;
        s = s.sibling;
      }
      throw Error(M(188));
    }
    if (n.return !== r.return) (n = i), (r = s);
    else {
      for (var o = !1, a = i.child; a; ) {
        if (a === n) {
          (o = !0), (n = i), (r = s);
          break;
        }
        if (a === r) {
          (o = !0), (r = i), (n = s);
          break;
        }
        a = a.sibling;
      }
      if (!o) {
        for (a = s.child; a; ) {
          if (a === n) {
            (o = !0), (n = s), (r = i);
            break;
          }
          if (a === r) {
            (o = !0), (r = s), (n = i);
            break;
          }
          a = a.sibling;
        }
        if (!o) throw Error(M(189));
      }
    }
    if (n.alternate !== r) throw Error(M(190));
  }
  if (n.tag !== 3) throw Error(M(188));
  return n.stateNode.current === n ? e : t;
}
function km(e) {
  return (e = _1(e)), e !== null ? Am(e) : null;
}
function Am(e) {
  if (e.tag === 5 || e.tag === 6) return e;
  for (e = e.child; e !== null; ) {
    var t = Am(e);
    if (t !== null) return t;
    e = e.sibling;
  }
  return null;
}
var Rm = rt.unstable_scheduleCallback,
  of = rt.unstable_cancelCallback,
  V1 = rt.unstable_shouldYield,
  z1 = rt.unstable_requestPaint,
  me = rt.unstable_now,
  B1 = rt.unstable_getCurrentPriorityLevel,
  lc = rt.unstable_ImmediatePriority,
  Mm = rt.unstable_UserBlockingPriority,
  Ao = rt.unstable_NormalPriority,
  U1 = rt.unstable_LowPriority,
  Dm = rt.unstable_IdlePriority,
  oa = null,
  Ft = null;
function $1(e) {
  if (Ft && typeof Ft.onCommitFiberRoot == "function")
    try {
      Ft.onCommitFiberRoot(oa, e, void 0, (e.current.flags & 128) === 128);
    } catch {}
}
var kt = Math.clz32 ? Math.clz32 : K1,
  W1 = Math.log,
  H1 = Math.LN2;
function K1(e) {
  return (e >>>= 0), e === 0 ? 32 : (31 - ((W1(e) / H1) | 0)) | 0;
}
var Bs = 64,
  Us = 4194304;
function Ni(e) {
  switch (e & -e) {
    case 1:
      return 1;
    case 2:
      return 2;
    case 4:
      return 4;
    case 8:
      return 8;
    case 16:
      return 16;
    case 32:
      return 32;
    case 64:
    case 128:
    case 256:
    case 512:
    case 1024:
    case 2048:
    case 4096:
    case 8192:
    case 16384:
    case 32768:
    case 65536:
    case 131072:
    case 262144:
    case 524288:
    case 1048576:
    case 2097152:
      return e & 4194240;
    case 4194304:
    case 8388608:
    case 16777216:
    case 33554432:
    case 67108864:
      return e & 130023424;
    case 134217728:
      return 134217728;
    case 268435456:
      return 268435456;
    case 536870912:
      return 536870912;
    case 1073741824:
      return 1073741824;
    default:
      return e;
  }
}
function Ro(e, t) {
  var n = e.pendingLanes;
  if (n === 0) return 0;
  var r = 0,
    i = e.suspendedLanes,
    s = e.pingedLanes,
    o = n & 268435455;
  if (o !== 0) {
    var a = o & ~i;
    a !== 0 ? (r = Ni(a)) : ((s &= o), s !== 0 && (r = Ni(s)));
  } else (o = n & ~i), o !== 0 ? (r = Ni(o)) : s !== 0 && (r = Ni(s));
  if (r === 0) return 0;
  if (
    t !== 0 &&
    t !== r &&
    !(t & i) &&
    ((i = r & -r), (s = t & -t), i >= s || (i === 16 && (s & 4194240) !== 0))
  )
    return t;
  if ((r & 4 && (r |= n & 16), (t = e.entangledLanes), t !== 0))
    for (e = e.entanglements, t &= r; 0 < t; )
      (n = 31 - kt(t)), (i = 1 << n), (r |= e[n]), (t &= ~i);
  return r;
}
function Q1(e, t) {
  switch (e) {
    case 1:
    case 2:
    case 4:
      return t + 250;
    case 8:
    case 16:
    case 32:
    case 64:
    case 128:
    case 256:
    case 512:
    case 1024:
    case 2048:
    case 4096:
    case 8192:
    case 16384:
    case 32768:
    case 65536:
    case 131072:
    case 262144:
    case 524288:
    case 1048576:
    case 2097152:
      return t + 5e3;
    case 4194304:
    case 8388608:
    case 16777216:
    case 33554432:
    case 67108864:
      return -1;
    case 134217728:
    case 268435456:
    case 536870912:
    case 1073741824:
      return -1;
    default:
      return -1;
  }
}
function G1(e, t) {
  for (
    var n = e.suspendedLanes,
      r = e.pingedLanes,
      i = e.expirationTimes,
      s = e.pendingLanes;
    0 < s;

  ) {
    var o = 31 - kt(s),
      a = 1 << o,
      l = i[o];
    l === -1
      ? (!(a & n) || a & r) && (i[o] = Q1(a, t))
      : l <= t && (e.expiredLanes |= a),
      (s &= ~a);
  }
}
function ql(e) {
  return (
    (e = e.pendingLanes & -1073741825),
    e !== 0 ? e : e & 1073741824 ? 1073741824 : 0
  );
}
function Nm() {
  var e = Bs;
  return (Bs <<= 1), !(Bs & 4194240) && (Bs = 64), e;
}
function Qa(e) {
  for (var t = [], n = 0; 31 > n; n++) t.push(e);
  return t;
}
function ks(e, t, n) {
  (e.pendingLanes |= t),
    t !== 536870912 && ((e.suspendedLanes = 0), (e.pingedLanes = 0)),
    (e = e.eventTimes),
    (t = 31 - kt(t)),
    (e[t] = n);
}
function q1(e, t) {
  var n = e.pendingLanes & ~t;
  (e.pendingLanes = t),
    (e.suspendedLanes = 0),
    (e.pingedLanes = 0),
    (e.expiredLanes &= t),
    (e.mutableReadLanes &= t),
    (e.entangledLanes &= t),
    (t = e.entanglements);
  var r = e.eventTimes;
  for (e = e.expirationTimes; 0 < n; ) {
    var i = 31 - kt(n),
      s = 1 << i;
    (t[i] = 0), (r[i] = -1), (e[i] = -1), (n &= ~s);
  }
}
function uc(e, t) {
  var n = (e.entangledLanes |= t);
  for (e = e.entanglements; n; ) {
    var r = 31 - kt(n),
      i = 1 << r;
    (i & t) | (e[r] & t) && (e[r] |= t), (n &= ~i);
  }
}
var X = 0;
function bm(e) {
  return (e &= -e), 1 < e ? (4 < e ? (e & 268435455 ? 16 : 536870912) : 4) : 1;
}
var Lm,
  cc,
  Om,
  jm,
  Im,
  Xl = !1,
  $s = [],
  Mn = null,
  Dn = null,
  Nn = null,
  Ji = new Map(),
  es = new Map(),
  wn = [],
  X1 =
    "mousedown mouseup touchcancel touchend touchstart auxclick dblclick pointercancel pointerdown pointerup dragend dragstart drop compositionend compositionstart keydown keypress keyup input textInput copy cut paste click change contextmenu reset submit".split(
      " "
    );
function af(e, t) {
  switch (e) {
    case "focusin":
    case "focusout":
      Mn = null;
      break;
    case "dragenter":
    case "dragleave":
      Dn = null;
      break;
    case "mouseover":
    case "mouseout":
      Nn = null;
      break;
    case "pointerover":
    case "pointerout":
      Ji.delete(t.pointerId);
      break;
    case "gotpointercapture":
    case "lostpointercapture":
      es.delete(t.pointerId);
  }
}
function wi(e, t, n, r, i, s) {
  return e === null || e.nativeEvent !== s
    ? ((e = {
        blockedOn: t,
        domEventName: n,
        eventSystemFlags: r,
        nativeEvent: s,
        targetContainers: [i],
      }),
      t !== null && ((t = Rs(t)), t !== null && cc(t)),
      e)
    : ((e.eventSystemFlags |= r),
      (t = e.targetContainers),
      i !== null && t.indexOf(i) === -1 && t.push(i),
      e);
}
function Y1(e, t, n, r, i) {
  switch (t) {
    case "focusin":
      return (Mn = wi(Mn, e, t, n, r, i)), !0;
    case "dragenter":
      return (Dn = wi(Dn, e, t, n, r, i)), !0;
    case "mouseover":
      return (Nn = wi(Nn, e, t, n, r, i)), !0;
    case "pointerover":
      var s = i.pointerId;
      return Ji.set(s, wi(Ji.get(s) || null, e, t, n, r, i)), !0;
    case "gotpointercapture":
      return (
        (s = i.pointerId), es.set(s, wi(es.get(s) || null, e, t, n, r, i)), !0
      );
  }
  return !1;
}
function Fm(e) {
  var t = Jn(e.target);
  if (t !== null) {
    var n = xr(t);
    if (n !== null) {
      if (((t = n.tag), t === 13)) {
        if (((t = Tm(n)), t !== null)) {
          (e.blockedOn = t),
            Im(e.priority, function () {
              Om(n);
            });
          return;
        }
      } else if (t === 3 && n.stateNode.current.memoizedState.isDehydrated) {
        e.blockedOn = n.tag === 3 ? n.stateNode.containerInfo : null;
        return;
      }
    }
  }
  e.blockedOn = null;
}
function lo(e) {
  if (e.blockedOn !== null) return !1;
  for (var t = e.targetContainers; 0 < t.length; ) {
    var n = Yl(e.domEventName, e.eventSystemFlags, t[0], e.nativeEvent);
    if (n === null) {
      n = e.nativeEvent;
      var r = new n.constructor(n.type, n);
      (Hl = r), n.target.dispatchEvent(r), (Hl = null);
    } else return (t = Rs(n)), t !== null && cc(t), (e.blockedOn = n), !1;
    t.shift();
  }
  return !0;
}
function lf(e, t, n) {
  lo(e) && n.delete(t);
}
function Z1() {
  (Xl = !1),
    Mn !== null && lo(Mn) && (Mn = null),
    Dn !== null && lo(Dn) && (Dn = null),
    Nn !== null && lo(Nn) && (Nn = null),
    Ji.forEach(lf),
    es.forEach(lf);
}
function Si(e, t) {
  e.blockedOn === t &&
    ((e.blockedOn = null),
    Xl ||
      ((Xl = !0),
      rt.unstable_scheduleCallback(rt.unstable_NormalPriority, Z1)));
}
function ts(e) {
  function t(i) {
    return Si(i, e);
  }
  if (0 < $s.length) {
    Si($s[0], e);
    for (var n = 1; n < $s.length; n++) {
      var r = $s[n];
      r.blockedOn === e && (r.blockedOn = null);
    }
  }
  for (
    Mn !== null && Si(Mn, e),
      Dn !== null && Si(Dn, e),
      Nn !== null && Si(Nn, e),
      Ji.forEach(t),
      es.forEach(t),
      n = 0;
    n < wn.length;
    n++
  )
    (r = wn[n]), r.blockedOn === e && (r.blockedOn = null);
  for (; 0 < wn.length && ((n = wn[0]), n.blockedOn === null); )
    Fm(n), n.blockedOn === null && wn.shift();
}
var Ur = ln.ReactCurrentBatchConfig,
  Mo = !0;
function J1(e, t, n, r) {
  var i = X,
    s = Ur.transition;
  Ur.transition = null;
  try {
    (X = 1), dc(e, t, n, r);
  } finally {
    (X = i), (Ur.transition = s);
  }
}
function ex(e, t, n, r) {
  var i = X,
    s = Ur.transition;
  Ur.transition = null;
  try {
    (X = 4), dc(e, t, n, r);
  } finally {
    (X = i), (Ur.transition = s);
  }
}
function dc(e, t, n, r) {
  if (Mo) {
    var i = Yl(e, t, n, r);
    if (i === null) rl(e, t, r, Do, n), af(e, r);
    else if (Y1(i, e, t, n, r)) r.stopPropagation();
    else if ((af(e, r), t & 4 && -1 < X1.indexOf(e))) {
      for (; i !== null; ) {
        var s = Rs(i);
        if (
          (s !== null && Lm(s),
          (s = Yl(e, t, n, r)),
          s === null && rl(e, t, r, Do, n),
          s === i)
        )
          break;
        i = s;
      }
      i !== null && r.stopPropagation();
    } else rl(e, t, r, null, n);
  }
}
var Do = null;
function Yl(e, t, n, r) {
  if (((Do = null), (e = ac(r)), (e = Jn(e)), e !== null))
    if (((t = xr(e)), t === null)) e = null;
    else if (((n = t.tag), n === 13)) {
      if (((e = Tm(t)), e !== null)) return e;
      e = null;
    } else if (n === 3) {
      if (t.stateNode.current.memoizedState.isDehydrated)
        return t.tag === 3 ? t.stateNode.containerInfo : null;
      e = null;
    } else t !== e && (e = null);
  return (Do = e), null;
}
function _m(e) {
  switch (e) {
    case "cancel":
    case "click":
    case "close":
    case "contextmenu":
    case "copy":
    case "cut":
    case "auxclick":
    case "dblclick":
    case "dragend":
    case "dragstart":
    case "drop":
    case "focusin":
    case "focusout":
    case "input":
    case "invalid":
    case "keydown":
    case "keypress":
    case "keyup":
    case "mousedown":
    case "mouseup":
    case "paste":
    case "pause":
    case "play":
    case "pointercancel":
    case "pointerdown":
    case "pointerup":
    case "ratechange":
    case "reset":
    case "resize":
    case "seeked":
    case "submit":
    case "touchcancel":
    case "touchend":
    case "touchstart":
    case "volumechange":
    case "change":
    case "selectionchange":
    case "textInput":
    case "compositionstart":
    case "compositionend":
    case "compositionupdate":
    case "beforeblur":
    case "afterblur":
    case "beforeinput":
    case "blur":
    case "fullscreenchange":
    case "focus":
    case "hashchange":
    case "popstate":
    case "select":
    case "selectstart":
      return 1;
    case "drag":
    case "dragenter":
    case "dragexit":
    case "dragleave":
    case "dragover":
    case "mousemove":
    case "mouseout":
    case "mouseover":
    case "pointermove":
    case "pointerout":
    case "pointerover":
    case "scroll":
    case "toggle":
    case "touchmove":
    case "wheel":
    case "mouseenter":
    case "mouseleave":
    case "pointerenter":
    case "pointerleave":
      return 4;
    case "message":
      switch (B1()) {
        case lc:
          return 1;
        case Mm:
          return 4;
        case Ao:
        case U1:
          return 16;
        case Dm:
          return 536870912;
        default:
          return 16;
      }
    default:
      return 16;
  }
}
var An = null,
  fc = null,
  uo = null;
function Vm() {
  if (uo) return uo;
  var e,
    t = fc,
    n = t.length,
    r,
    i = "value" in An ? An.value : An.textContent,
    s = i.length;
  for (e = 0; e < n && t[e] === i[e]; e++);
  var o = n - e;
  for (r = 1; r <= o && t[n - r] === i[s - r]; r++);
  return (uo = i.slice(e, 1 < r ? 1 - r : void 0));
}
function co(e) {
  var t = e.keyCode;
  return (
    "charCode" in e
      ? ((e = e.charCode), e === 0 && t === 13 && (e = 13))
      : (e = t),
    e === 10 && (e = 13),
    32 <= e || e === 13 ? e : 0
  );
}
function Ws() {
  return !0;
}
function uf() {
  return !1;
}
function ot(e) {
  function t(n, r, i, s, o) {
    (this._reactName = n),
      (this._targetInst = i),
      (this.type = r),
      (this.nativeEvent = s),
      (this.target = o),
      (this.currentTarget = null);
    for (var a in e)
      e.hasOwnProperty(a) && ((n = e[a]), (this[a] = n ? n(s) : s[a]));
    return (
      (this.isDefaultPrevented = (
        s.defaultPrevented != null ? s.defaultPrevented : s.returnValue === !1
      )
        ? Ws
        : uf),
      (this.isPropagationStopped = uf),
      this
    );
  }
  return (
    ce(t.prototype, {
      preventDefault: function () {
        this.defaultPrevented = !0;
        var n = this.nativeEvent;
        n &&
          (n.preventDefault
            ? n.preventDefault()
            : typeof n.returnValue != "unknown" && (n.returnValue = !1),
          (this.isDefaultPrevented = Ws));
      },
      stopPropagation: function () {
        var n = this.nativeEvent;
        n &&
          (n.stopPropagation
            ? n.stopPropagation()
            : typeof n.cancelBubble != "unknown" && (n.cancelBubble = !0),
          (this.isPropagationStopped = Ws));
      },
      persist: function () {},
      isPersistent: Ws,
    }),
    t
  );
}
var hi = {
    eventPhase: 0,
    bubbles: 0,
    cancelable: 0,
    timeStamp: function (e) {
      return e.timeStamp || Date.now();
    },
    defaultPrevented: 0,
    isTrusted: 0,
  },
  hc = ot(hi),
  As = ce({}, hi, { view: 0, detail: 0 }),
  tx = ot(As),
  Ga,
  qa,
  Pi,
  aa = ce({}, As, {
    screenX: 0,
    screenY: 0,
    clientX: 0,
    clientY: 0,
    pageX: 0,
    pageY: 0,
    ctrlKey: 0,
    shiftKey: 0,
    altKey: 0,
    metaKey: 0,
    getModifierState: pc,
    button: 0,
    buttons: 0,
    relatedTarget: function (e) {
      return e.relatedTarget === void 0
        ? e.fromElement === e.srcElement
          ? e.toElement
          : e.fromElement
        : e.relatedTarget;
    },
    movementX: function (e) {
      return "movementX" in e
        ? e.movementX
        : (e !== Pi &&
            (Pi && e.type === "mousemove"
              ? ((Ga = e.screenX - Pi.screenX), (qa = e.screenY - Pi.screenY))
              : (qa = Ga = 0),
            (Pi = e)),
          Ga);
    },
    movementY: function (e) {
      return "movementY" in e ? e.movementY : qa;
    },
  }),
  cf = ot(aa),
  nx = ce({}, aa, { dataTransfer: 0 }),
  rx = ot(nx),
  ix = ce({}, As, { relatedTarget: 0 }),
  Xa = ot(ix),
  sx = ce({}, hi, { animationName: 0, elapsedTime: 0, pseudoElement: 0 }),
  ox = ot(sx),
  ax = ce({}, hi, {
    clipboardData: function (e) {
      return "clipboardData" in e ? e.clipboardData : window.clipboardData;
    },
  }),
  lx = ot(ax),
  ux = ce({}, hi, { data: 0 }),
  df = ot(ux),
  cx = {
    Esc: "Escape",
    Spacebar: " ",
    Left: "ArrowLeft",
    Up: "ArrowUp",
    Right: "ArrowRight",
    Down: "ArrowDown",
    Del: "Delete",
    Win: "OS",
    Menu: "ContextMenu",
    Apps: "ContextMenu",
    Scroll: "ScrollLock",
    MozPrintableKey: "Unidentified",
  },
  dx = {
    8: "Backspace",
    9: "Tab",
    12: "Clear",
    13: "Enter",
    16: "Shift",
    17: "Control",
    18: "Alt",
    19: "Pause",
    20: "CapsLock",
    27: "Escape",
    32: " ",
    33: "PageUp",
    34: "PageDown",
    35: "End",
    36: "Home",
    37: "ArrowLeft",
    38: "ArrowUp",
    39: "ArrowRight",
    40: "ArrowDown",
    45: "Insert",
    46: "Delete",
    112: "F1",
    113: "F2",
    114: "F3",
    115: "F4",
    116: "F5",
    117: "F6",
    118: "F7",
    119: "F8",
    120: "F9",
    121: "F10",
    122: "F11",
    123: "F12",
    144: "NumLock",
    145: "ScrollLock",
    224: "Meta",
  },
  fx = {
    Alt: "altKey",
    Control: "ctrlKey",
    Meta: "metaKey",
    Shift: "shiftKey",
  };
function hx(e) {
  var t = this.nativeEvent;
  return t.getModifierState ? t.getModifierState(e) : (e = fx[e]) ? !!t[e] : !1;
}
function pc() {
  return hx;
}
var px = ce({}, As, {
    key: function (e) {
      if (e.key) {
        var t = cx[e.key] || e.key;
        if (t !== "Unidentified") return t;
      }
      return e.type === "keypress"
        ? ((e = co(e)), e === 13 ? "Enter" : String.fromCharCode(e))
        : e.type === "keydown" || e.type === "keyup"
        ? dx[e.keyCode] || "Unidentified"
        : "";
    },
    code: 0,
    location: 0,
    ctrlKey: 0,
    shiftKey: 0,
    altKey: 0,
    metaKey: 0,
    repeat: 0,
    locale: 0,
    getModifierState: pc,
    charCode: function (e) {
      return e.type === "keypress" ? co(e) : 0;
    },
    keyCode: function (e) {
      return e.type === "keydown" || e.type === "keyup" ? e.keyCode : 0;
    },
    which: function (e) {
      return e.type === "keypress"
        ? co(e)
        : e.type === "keydown" || e.type === "keyup"
        ? e.keyCode
        : 0;
    },
  }),
  mx = ot(px),
  gx = ce({}, aa, {
    pointerId: 0,
    width: 0,
    height: 0,
    pressure: 0,
    tangentialPressure: 0,
    tiltX: 0,
    tiltY: 0,
    twist: 0,
    pointerType: 0,
    isPrimary: 0,
  }),
  ff = ot(gx),
  yx = ce({}, As, {
    touches: 0,
    targetTouches: 0,
    changedTouches: 0,
    altKey: 0,
    metaKey: 0,
    ctrlKey: 0,
    shiftKey: 0,
    getModifierState: pc,
  }),
  vx = ot(yx),
  xx = ce({}, hi, { propertyName: 0, elapsedTime: 0, pseudoElement: 0 }),
  wx = ot(xx),
  Sx = ce({}, aa, {
    deltaX: function (e) {
      return "deltaX" in e ? e.deltaX : "wheelDeltaX" in e ? -e.wheelDeltaX : 0;
    },
    deltaY: function (e) {
      return "deltaY" in e
        ? e.deltaY
        : "wheelDeltaY" in e
        ? -e.wheelDeltaY
        : "wheelDelta" in e
        ? -e.wheelDelta
        : 0;
    },
    deltaZ: 0,
    deltaMode: 0,
  }),
  Px = ot(Sx),
  Cx = [9, 13, 27, 32],
  mc = tn && "CompositionEvent" in window,
  _i = null;
tn && "documentMode" in document && (_i = document.documentMode);
var Ex = tn && "TextEvent" in window && !_i,
  zm = tn && (!mc || (_i && 8 < _i && 11 >= _i)),
  hf = " ",
  pf = !1;
function Bm(e, t) {
  switch (e) {
    case "keyup":
      return Cx.indexOf(t.keyCode) !== -1;
    case "keydown":
      return t.keyCode !== 229;
    case "keypress":
    case "mousedown":
    case "focusout":
      return !0;
    default:
      return !1;
  }
}
function Um(e) {
  return (e = e.detail), typeof e == "object" && "data" in e ? e.data : null;
}
var Er = !1;
function Tx(e, t) {
  switch (e) {
    case "compositionend":
      return Um(t);
    case "keypress":
      return t.which !== 32 ? null : ((pf = !0), hf);
    case "textInput":
      return (e = t.data), e === hf && pf ? null : e;
    default:
      return null;
  }
}
function kx(e, t) {
  if (Er)
    return e === "compositionend" || (!mc && Bm(e, t))
      ? ((e = Vm()), (uo = fc = An = null), (Er = !1), e)
      : null;
  switch (e) {
    case "paste":
      return null;
    case "keypress":
      if (!(t.ctrlKey || t.altKey || t.metaKey) || (t.ctrlKey && t.altKey)) {
        if (t.char && 1 < t.char.length) return t.char;
        if (t.which) return String.fromCharCode(t.which);
      }
      return null;
    case "compositionend":
      return zm && t.locale !== "ko" ? null : t.data;
    default:
      return null;
  }
}
var Ax = {
  color: !0,
  date: !0,
  datetime: !0,
  "datetime-local": !0,
  email: !0,
  month: !0,
  number: !0,
  password: !0,
  range: !0,
  search: !0,
  tel: !0,
  text: !0,
  time: !0,
  url: !0,
  week: !0,
};
function mf(e) {
  var t = e && e.nodeName && e.nodeName.toLowerCase();
  return t === "input" ? !!Ax[e.type] : t === "textarea";
}
function $m(e, t, n, r) {
  wm(r),
    (t = No(t, "onChange")),
    0 < t.length &&
      ((n = new hc("onChange", "change", null, n, r)),
      e.push({ event: n, listeners: t }));
}
var Vi = null,
  ns = null;
function Rx(e) {
  eg(e, 0);
}
function la(e) {
  var t = Ar(e);
  if (hm(t)) return e;
}
function Mx(e, t) {
  if (e === "change") return t;
}
var Wm = !1;
if (tn) {
  var Ya;
  if (tn) {
    var Za = "oninput" in document;
    if (!Za) {
      var gf = document.createElement("div");
      gf.setAttribute("oninput", "return;"),
        (Za = typeof gf.oninput == "function");
    }
    Ya = Za;
  } else Ya = !1;
  Wm = Ya && (!document.documentMode || 9 < document.documentMode);
}
function yf() {
  Vi && (Vi.detachEvent("onpropertychange", Hm), (ns = Vi = null));
}
function Hm(e) {
  if (e.propertyName === "value" && la(ns)) {
    var t = [];
    $m(t, ns, e, ac(e)), Em(Rx, t);
  }
}
function Dx(e, t, n) {
  e === "focusin"
    ? (yf(), (Vi = t), (ns = n), Vi.attachEvent("onpropertychange", Hm))
    : e === "focusout" && yf();
}
function Nx(e) {
  if (e === "selectionchange" || e === "keyup" || e === "keydown")
    return la(ns);
}
function bx(e, t) {
  if (e === "click") return la(t);
}
function Lx(e, t) {
  if (e === "input" || e === "change") return la(t);
}
function Ox(e, t) {
  return (e === t && (e !== 0 || 1 / e === 1 / t)) || (e !== e && t !== t);
}
var Mt = typeof Object.is == "function" ? Object.is : Ox;
function rs(e, t) {
  if (Mt(e, t)) return !0;
  if (typeof e != "object" || e === null || typeof t != "object" || t === null)
    return !1;
  var n = Object.keys(e),
    r = Object.keys(t);
  if (n.length !== r.length) return !1;
  for (r = 0; r < n.length; r++) {
    var i = n[r];
    if (!Ll.call(t, i) || !Mt(e[i], t[i])) return !1;
  }
  return !0;
}
function vf(e) {
  for (; e && e.firstChild; ) e = e.firstChild;
  return e;
}
function xf(e, t) {
  var n = vf(e);
  e = 0;
  for (var r; n; ) {
    if (n.nodeType === 3) {
      if (((r = e + n.textContent.length), e <= t && r >= t))
        return { node: n, offset: t - e };
      e = r;
    }
    e: {
      for (; n; ) {
        if (n.nextSibling) {
          n = n.nextSibling;
          break e;
        }
        n = n.parentNode;
      }
      n = void 0;
    }
    n = vf(n);
  }
}
function Km(e, t) {
  return e && t
    ? e === t
      ? !0
      : e && e.nodeType === 3
      ? !1
      : t && t.nodeType === 3
      ? Km(e, t.parentNode)
      : "contains" in e
      ? e.contains(t)
      : e.compareDocumentPosition
      ? !!(e.compareDocumentPosition(t) & 16)
      : !1
    : !1;
}
function Qm() {
  for (var e = window, t = Eo(); t instanceof e.HTMLIFrameElement; ) {
    try {
      var n = typeof t.contentWindow.location.href == "string";
    } catch {
      n = !1;
    }
    if (n) e = t.contentWindow;
    else break;
    t = Eo(e.document);
  }
  return t;
}
function gc(e) {
  var t = e && e.nodeName && e.nodeName.toLowerCase();
  return (
    t &&
    ((t === "input" &&
      (e.type === "text" ||
        e.type === "search" ||
        e.type === "tel" ||
        e.type === "url" ||
        e.type === "password")) ||
      t === "textarea" ||
      e.contentEditable === "true")
  );
}
function jx(e) {
  var t = Qm(),
    n = e.focusedElem,
    r = e.selectionRange;
  if (
    t !== n &&
    n &&
    n.ownerDocument &&
    Km(n.ownerDocument.documentElement, n)
  ) {
    if (r !== null && gc(n)) {
      if (
        ((t = r.start),
        (e = r.end),
        e === void 0 && (e = t),
        "selectionStart" in n)
      )
        (n.selectionStart = t), (n.selectionEnd = Math.min(e, n.value.length));
      else if (
        ((e = ((t = n.ownerDocument || document) && t.defaultView) || window),
        e.getSelection)
      ) {
        e = e.getSelection();
        var i = n.textContent.length,
          s = Math.min(r.start, i);
        (r = r.end === void 0 ? s : Math.min(r.end, i)),
          !e.extend && s > r && ((i = r), (r = s), (s = i)),
          (i = xf(n, s));
        var o = xf(n, r);
        i &&
          o &&
          (e.rangeCount !== 1 ||
            e.anchorNode !== i.node ||
            e.anchorOffset !== i.offset ||
            e.focusNode !== o.node ||
            e.focusOffset !== o.offset) &&
          ((t = t.createRange()),
          t.setStart(i.node, i.offset),
          e.removeAllRanges(),
          s > r
            ? (e.addRange(t), e.extend(o.node, o.offset))
            : (t.setEnd(o.node, o.offset), e.addRange(t)));
      }
    }
    for (t = [], e = n; (e = e.parentNode); )
      e.nodeType === 1 &&
        t.push({ element: e, left: e.scrollLeft, top: e.scrollTop });
    for (typeof n.focus == "function" && n.focus(), n = 0; n < t.length; n++)
      (e = t[n]),
        (e.element.scrollLeft = e.left),
        (e.element.scrollTop = e.top);
  }
}
var Ix = tn && "documentMode" in document && 11 >= document.documentMode,
  Tr = null,
  Zl = null,
  zi = null,
  Jl = !1;
function wf(e, t, n) {
  var r = n.window === n ? n.document : n.nodeType === 9 ? n : n.ownerDocument;
  Jl ||
    Tr == null ||
    Tr !== Eo(r) ||
    ((r = Tr),
    "selectionStart" in r && gc(r)
      ? (r = { start: r.selectionStart, end: r.selectionEnd })
      : ((r = (
          (r.ownerDocument && r.ownerDocument.defaultView) ||
          window
        ).getSelection()),
        (r = {
          anchorNode: r.anchorNode,
          anchorOffset: r.anchorOffset,
          focusNode: r.focusNode,
          focusOffset: r.focusOffset,
        })),
    (zi && rs(zi, r)) ||
      ((zi = r),
      (r = No(Zl, "onSelect")),
      0 < r.length &&
        ((t = new hc("onSelect", "select", null, t, n)),
        e.push({ event: t, listeners: r }),
        (t.target = Tr))));
}
function Hs(e, t) {
  var n = {};
  return (
    (n[e.toLowerCase()] = t.toLowerCase()),
    (n["Webkit" + e] = "webkit" + t),
    (n["Moz" + e] = "moz" + t),
    n
  );
}
var kr = {
    animationend: Hs("Animation", "AnimationEnd"),
    animationiteration: Hs("Animation", "AnimationIteration"),
    animationstart: Hs("Animation", "AnimationStart"),
    transitionend: Hs("Transition", "TransitionEnd"),
  },
  Ja = {},
  Gm = {};
tn &&
  ((Gm = document.createElement("div").style),
  "AnimationEvent" in window ||
    (delete kr.animationend.animation,
    delete kr.animationiteration.animation,
    delete kr.animationstart.animation),
  "TransitionEvent" in window || delete kr.transitionend.transition);
function ua(e) {
  if (Ja[e]) return Ja[e];
  if (!kr[e]) return e;
  var t = kr[e],
    n;
  for (n in t) if (t.hasOwnProperty(n) && n in Gm) return (Ja[e] = t[n]);
  return e;
}
var qm = ua("animationend"),
  Xm = ua("animationiteration"),
  Ym = ua("animationstart"),
  Zm = ua("transitionend"),
  Jm = new Map(),
  Sf =
    "abort auxClick cancel canPlay canPlayThrough click close contextMenu copy cut drag dragEnd dragEnter dragExit dragLeave dragOver dragStart drop durationChange emptied encrypted ended error gotPointerCapture input invalid keyDown keyPress keyUp load loadedData loadedMetadata loadStart lostPointerCapture mouseDown mouseMove mouseOut mouseOver mouseUp paste pause play playing pointerCancel pointerDown pointerMove pointerOut pointerOver pointerUp progress rateChange reset resize seeked seeking stalled submit suspend timeUpdate touchCancel touchEnd touchStart volumeChange scroll toggle touchMove waiting wheel".split(
      " "
    );
function $n(e, t) {
  Jm.set(e, t), vr(t, [e]);
}
for (var el = 0; el < Sf.length; el++) {
  var tl = Sf[el],
    Fx = tl.toLowerCase(),
    _x = tl[0].toUpperCase() + tl.slice(1);
  $n(Fx, "on" + _x);
}
$n(qm, "onAnimationEnd");
$n(Xm, "onAnimationIteration");
$n(Ym, "onAnimationStart");
$n("dblclick", "onDoubleClick");
$n("focusin", "onFocus");
$n("focusout", "onBlur");
$n(Zm, "onTransitionEnd");
ti("onMouseEnter", ["mouseout", "mouseover"]);
ti("onMouseLeave", ["mouseout", "mouseover"]);
ti("onPointerEnter", ["pointerout", "pointerover"]);
ti("onPointerLeave", ["pointerout", "pointerover"]);
vr(
  "onChange",
  "change click focusin focusout input keydown keyup selectionchange".split(" ")
);
vr(
  "onSelect",
  "focusout contextmenu dragend focusin keydown keyup mousedown mouseup selectionchange".split(
    " "
  )
);
vr("onBeforeInput", ["compositionend", "keypress", "textInput", "paste"]);
vr(
  "onCompositionEnd",
  "compositionend focusout keydown keypress keyup mousedown".split(" ")
);
vr(
  "onCompositionStart",
  "compositionstart focusout keydown keypress keyup mousedown".split(" ")
);
vr(
  "onCompositionUpdate",
  "compositionupdate focusout keydown keypress keyup mousedown".split(" ")
);
var bi =
    "abort canplay canplaythrough durationchange emptied encrypted ended error loadeddata loadedmetadata loadstart pause play playing progress ratechange resize seeked seeking stalled suspend timeupdate volumechange waiting".split(
      " "
    ),
  Vx = new Set("cancel close invalid load scroll toggle".split(" ").concat(bi));
function Pf(e, t, n) {
  var r = e.type || "unknown-event";
  (e.currentTarget = n), F1(r, t, void 0, e), (e.currentTarget = null);
}
function eg(e, t) {
  t = (t & 4) !== 0;
  for (var n = 0; n < e.length; n++) {
    var r = e[n],
      i = r.event;
    r = r.listeners;
    e: {
      var s = void 0;
      if (t)
        for (var o = r.length - 1; 0 <= o; o--) {
          var a = r[o],
            l = a.instance,
            u = a.currentTarget;
          if (((a = a.listener), l !== s && i.isPropagationStopped())) break e;
          Pf(i, a, u), (s = l);
        }
      else
        for (o = 0; o < r.length; o++) {
          if (
            ((a = r[o]),
            (l = a.instance),
            (u = a.currentTarget),
            (a = a.listener),
            l !== s && i.isPropagationStopped())
          )
            break e;
          Pf(i, a, u), (s = l);
        }
    }
  }
  if (ko) throw ((e = Gl), (ko = !1), (Gl = null), e);
}
function ne(e, t) {
  var n = t[iu];
  n === void 0 && (n = t[iu] = new Set());
  var r = e + "__bubble";
  n.has(r) || (tg(t, e, 2, !1), n.add(r));
}
function nl(e, t, n) {
  var r = 0;
  t && (r |= 4), tg(n, e, r, t);
}
var Ks = "_reactListening" + Math.random().toString(36).slice(2);
function is(e) {
  if (!e[Ks]) {
    (e[Ks] = !0),
      lm.forEach(function (n) {
        n !== "selectionchange" && (Vx.has(n) || nl(n, !1, e), nl(n, !0, e));
      });
    var t = e.nodeType === 9 ? e : e.ownerDocument;
    t === null || t[Ks] || ((t[Ks] = !0), nl("selectionchange", !1, t));
  }
}
function tg(e, t, n, r) {
  switch (_m(t)) {
    case 1:
      var i = J1;
      break;
    case 4:
      i = ex;
      break;
    default:
      i = dc;
  }
  (n = i.bind(null, t, n, e)),
    (i = void 0),
    !Ql ||
      (t !== "touchstart" && t !== "touchmove" && t !== "wheel") ||
      (i = !0),
    r
      ? i !== void 0
        ? e.addEventListener(t, n, { capture: !0, passive: i })
        : e.addEventListener(t, n, !0)
      : i !== void 0
      ? e.addEventListener(t, n, { passive: i })
      : e.addEventListener(t, n, !1);
}
function rl(e, t, n, r, i) {
  var s = r;
  if (!(t & 1) && !(t & 2) && r !== null)
    e: for (;;) {
      if (r === null) return;
      var o = r.tag;
      if (o === 3 || o === 4) {
        var a = r.stateNode.containerInfo;
        if (a === i || (a.nodeType === 8 && a.parentNode === i)) break;
        if (o === 4)
          for (o = r.return; o !== null; ) {
            var l = o.tag;
            if (
              (l === 3 || l === 4) &&
              ((l = o.stateNode.containerInfo),
              l === i || (l.nodeType === 8 && l.parentNode === i))
            )
              return;
            o = o.return;
          }
        for (; a !== null; ) {
          if (((o = Jn(a)), o === null)) return;
          if (((l = o.tag), l === 5 || l === 6)) {
            r = s = o;
            continue e;
          }
          a = a.parentNode;
        }
      }
      r = r.return;
    }
  Em(function () {
    var u = s,
      c = ac(n),
      d = [];
    e: {
      var f = Jm.get(e);
      if (f !== void 0) {
        var v = hc,
          y = e;
        switch (e) {
          case "keypress":
            if (co(n) === 0) break e;
          case "keydown":
          case "keyup":
            v = mx;
            break;
          case "focusin":
            (y = "focus"), (v = Xa);
            break;
          case "focusout":
            (y = "blur"), (v = Xa);
            break;
          case "beforeblur":
          case "afterblur":
            v = Xa;
            break;
          case "click":
            if (n.button === 2) break e;
          case "auxclick":
          case "dblclick":
          case "mousedown":
          case "mousemove":
          case "mouseup":
          case "mouseout":
          case "mouseover":
          case "contextmenu":
            v = cf;
            break;
          case "drag":
          case "dragend":
          case "dragenter":
          case "dragexit":
          case "dragleave":
          case "dragover":
          case "dragstart":
          case "drop":
            v = rx;
            break;
          case "touchcancel":
          case "touchend":
          case "touchmove":
          case "touchstart":
            v = vx;
            break;
          case qm:
          case Xm:
          case Ym:
            v = ox;
            break;
          case Zm:
            v = wx;
            break;
          case "scroll":
            v = tx;
            break;
          case "wheel":
            v = Px;
            break;
          case "copy":
          case "cut":
          case "paste":
            v = lx;
            break;
          case "gotpointercapture":
          case "lostpointercapture":
          case "pointercancel":
          case "pointerdown":
          case "pointermove":
          case "pointerout":
          case "pointerover":
          case "pointerup":
            v = ff;
        }
        var m = (t & 4) !== 0,
          x = !m && e === "scroll",
          h = m ? (f !== null ? f + "Capture" : null) : f;
        m = [];
        for (var p = u, g; p !== null; ) {
          g = p;
          var S = g.stateNode;
          if (
            (g.tag === 5 &&
              S !== null &&
              ((g = S),
              h !== null && ((S = Zi(p, h)), S != null && m.push(ss(p, S, g)))),
            x)
          )
            break;
          p = p.return;
        }
        0 < m.length &&
          ((f = new v(f, y, null, n, c)), d.push({ event: f, listeners: m }));
      }
    }
    if (!(t & 7)) {
      e: {
        if (
          ((f = e === "mouseover" || e === "pointerover"),
          (v = e === "mouseout" || e === "pointerout"),
          f &&
            n !== Hl &&
            (y = n.relatedTarget || n.fromElement) &&
            (Jn(y) || y[nn]))
        )
          break e;
        if (
          (v || f) &&
          ((f =
            c.window === c
              ? c
              : (f = c.ownerDocument)
              ? f.defaultView || f.parentWindow
              : window),
          v
            ? ((y = n.relatedTarget || n.toElement),
              (v = u),
              (y = y ? Jn(y) : null),
              y !== null &&
                ((x = xr(y)), y !== x || (y.tag !== 5 && y.tag !== 6)) &&
                (y = null))
            : ((v = null), (y = u)),
          v !== y)
        ) {
          if (
            ((m = cf),
            (S = "onMouseLeave"),
            (h = "onMouseEnter"),
            (p = "mouse"),
            (e === "pointerout" || e === "pointerover") &&
              ((m = ff),
              (S = "onPointerLeave"),
              (h = "onPointerEnter"),
              (p = "pointer")),
            (x = v == null ? f : Ar(v)),
            (g = y == null ? f : Ar(y)),
            (f = new m(S, p + "leave", v, n, c)),
            (f.target = x),
            (f.relatedTarget = g),
            (S = null),
            Jn(c) === u &&
              ((m = new m(h, p + "enter", y, n, c)),
              (m.target = g),
              (m.relatedTarget = x),
              (S = m)),
            (x = S),
            v && y)
          )
            t: {
              for (m = v, h = y, p = 0, g = m; g; g = Sr(g)) p++;
              for (g = 0, S = h; S; S = Sr(S)) g++;
              for (; 0 < p - g; ) (m = Sr(m)), p--;
              for (; 0 < g - p; ) (h = Sr(h)), g--;
              for (; p--; ) {
                if (m === h || (h !== null && m === h.alternate)) break t;
                (m = Sr(m)), (h = Sr(h));
              }
              m = null;
            }
          else m = null;
          v !== null && Cf(d, f, v, m, !1),
            y !== null && x !== null && Cf(d, x, y, m, !0);
        }
      }
      e: {
        if (
          ((f = u ? Ar(u) : window),
          (v = f.nodeName && f.nodeName.toLowerCase()),
          v === "select" || (v === "input" && f.type === "file"))
        )
          var C = Mx;
        else if (mf(f))
          if (Wm) C = Lx;
          else {
            C = Nx;
            var k = Dx;
          }
        else
          (v = f.nodeName) &&
            v.toLowerCase() === "input" &&
            (f.type === "checkbox" || f.type === "radio") &&
            (C = bx);
        if (C && (C = C(e, u))) {
          $m(d, C, n, c);
          break e;
        }
        k && k(e, f, u),
          e === "focusout" &&
            (k = f._wrapperState) &&
            k.controlled &&
            f.type === "number" &&
            zl(f, "number", f.value);
      }
      switch (((k = u ? Ar(u) : window), e)) {
        case "focusin":
          (mf(k) || k.contentEditable === "true") &&
            ((Tr = k), (Zl = u), (zi = null));
          break;
        case "focusout":
          zi = Zl = Tr = null;
          break;
        case "mousedown":
          Jl = !0;
          break;
        case "contextmenu":
        case "mouseup":
        case "dragend":
          (Jl = !1), wf(d, n, c);
          break;
        case "selectionchange":
          if (Ix) break;
        case "keydown":
        case "keyup":
          wf(d, n, c);
      }
      var T;
      if (mc)
        e: {
          switch (e) {
            case "compositionstart":
              var E = "onCompositionStart";
              break e;
            case "compositionend":
              E = "onCompositionEnd";
              break e;
            case "compositionupdate":
              E = "onCompositionUpdate";
              break e;
          }
          E = void 0;
        }
      else
        Er
          ? Bm(e, n) && (E = "onCompositionEnd")
          : e === "keydown" && n.keyCode === 229 && (E = "onCompositionStart");
      E &&
        (zm &&
          n.locale !== "ko" &&
          (Er || E !== "onCompositionStart"
            ? E === "onCompositionEnd" && Er && (T = Vm())
            : ((An = c),
              (fc = "value" in An ? An.value : An.textContent),
              (Er = !0))),
        (k = No(u, E)),
        0 < k.length &&
          ((E = new df(E, e, null, n, c)),
          d.push({ event: E, listeners: k }),
          T ? (E.data = T) : ((T = Um(n)), T !== null && (E.data = T)))),
        (T = Ex ? Tx(e, n) : kx(e, n)) &&
          ((u = No(u, "onBeforeInput")),
          0 < u.length &&
            ((c = new df("onBeforeInput", "beforeinput", null, n, c)),
            d.push({ event: c, listeners: u }),
            (c.data = T)));
    }
    eg(d, t);
  });
}
function ss(e, t, n) {
  return { instance: e, listener: t, currentTarget: n };
}
function No(e, t) {
  for (var n = t + "Capture", r = []; e !== null; ) {
    var i = e,
      s = i.stateNode;
    i.tag === 5 &&
      s !== null &&
      ((i = s),
      (s = Zi(e, n)),
      s != null && r.unshift(ss(e, s, i)),
      (s = Zi(e, t)),
      s != null && r.push(ss(e, s, i))),
      (e = e.return);
  }
  return r;
}
function Sr(e) {
  if (e === null) return null;
  do e = e.return;
  while (e && e.tag !== 5);
  return e || null;
}
function Cf(e, t, n, r, i) {
  for (var s = t._reactName, o = []; n !== null && n !== r; ) {
    var a = n,
      l = a.alternate,
      u = a.stateNode;
    if (l !== null && l === r) break;
    a.tag === 5 &&
      u !== null &&
      ((a = u),
      i
        ? ((l = Zi(n, s)), l != null && o.unshift(ss(n, l, a)))
        : i || ((l = Zi(n, s)), l != null && o.push(ss(n, l, a)))),
      (n = n.return);
  }
  o.length !== 0 && e.push({ event: t, listeners: o });
}
var zx = /\r\n?/g,
  Bx = /\u0000|\uFFFD/g;
function Ef(e) {
  return (typeof e == "string" ? e : "" + e)
    .replace(
      zx,
      `
  `
    )
    .replace(Bx, "");
}
function Qs(e, t, n) {
  if (((t = Ef(t)), Ef(e) !== t && n)) throw Error(M(425));
}
function bo() {}
var eu = null,
  tu = null;
function nu(e, t) {
  return (
    e === "textarea" ||
    e === "noscript" ||
    typeof t.children == "string" ||
    typeof t.children == "number" ||
    (typeof t.dangerouslySetInnerHTML == "object" &&
      t.dangerouslySetInnerHTML !== null &&
      t.dangerouslySetInnerHTML.__html != null)
  );
}
var ru = typeof setTimeout == "function" ? setTimeout : void 0,
  Ux = typeof clearTimeout == "function" ? clearTimeout : void 0,
  Tf = typeof Promise == "function" ? Promise : void 0,
  $x =
    typeof queueMicrotask == "function"
      ? queueMicrotask
      : typeof Tf < "u"
      ? function (e) {
          return Tf.resolve(null).then(e).catch(Wx);
        }
      : ru;
function Wx(e) {
  setTimeout(function () {
    throw e;
  });
}
function il(e, t) {
  var n = t,
    r = 0;
  do {
    var i = n.nextSibling;
    if ((e.removeChild(n), i && i.nodeType === 8))
      if (((n = i.data), n === "/$")) {
        if (r === 0) {
          e.removeChild(i), ts(t);
          return;
        }
        r--;
      } else (n !== "$" && n !== "$?" && n !== "$!") || r++;
    n = i;
  } while (n);
  ts(t);
}
function bn(e) {
  for (; e != null; e = e.nextSibling) {
    var t = e.nodeType;
    if (t === 1 || t === 3) break;
    if (t === 8) {
      if (((t = e.data), t === "$" || t === "$!" || t === "$?")) break;
      if (t === "/$") return null;
    }
  }
  return e;
}
function kf(e) {
  e = e.previousSibling;
  for (var t = 0; e; ) {
    if (e.nodeType === 8) {
      var n = e.data;
      if (n === "$" || n === "$!" || n === "$?") {
        if (t === 0) return e;
        t--;
      } else n === "/$" && t++;
    }
    e = e.previousSibling;
  }
  return null;
}
var pi = Math.random().toString(36).slice(2),
  It = "__reactFiber$" + pi,
  os = "__reactProps$" + pi,
  nn = "__reactContainer$" + pi,
  iu = "__reactEvents$" + pi,
  Hx = "__reactListeners$" + pi,
  Kx = "__reactHandles$" + pi;
function Jn(e) {
  var t = e[It];
  if (t) return t;
  for (var n = e.parentNode; n; ) {
    if ((t = n[nn] || n[It])) {
      if (
        ((n = t.alternate),
        t.child !== null || (n !== null && n.child !== null))
      )
        for (e = kf(e); e !== null; ) {
          if ((n = e[It])) return n;
          e = kf(e);
        }
      return t;
    }
    (e = n), (n = e.parentNode);
  }
  return null;
}
function Rs(e) {
  return (
    (e = e[It] || e[nn]),
    !e || (e.tag !== 5 && e.tag !== 6 && e.tag !== 13 && e.tag !== 3) ? null : e
  );
}
function Ar(e) {
  if (e.tag === 5 || e.tag === 6) return e.stateNode;
  throw Error(M(33));
}
function ca(e) {
  return e[os] || null;
}
var su = [],
  Rr = -1;
function Wn(e) {
  return { current: e };
}
function re(e) {
  0 > Rr || ((e.current = su[Rr]), (su[Rr] = null), Rr--);
}
function ee(e, t) {
  Rr++, (su[Rr] = e.current), (e.current = t);
}
var zn = {},
  Fe = Wn(zn),
  Ge = Wn(!1),
  dr = zn;
function ni(e, t) {
  var n = e.type.contextTypes;
  if (!n) return zn;
  var r = e.stateNode;
  if (r && r.__reactInternalMemoizedUnmaskedChildContext === t)
    return r.__reactInternalMemoizedMaskedChildContext;
  var i = {},
    s;
  for (s in n) i[s] = t[s];
  return (
    r &&
      ((e = e.stateNode),
      (e.__reactInternalMemoizedUnmaskedChildContext = t),
      (e.__reactInternalMemoizedMaskedChildContext = i)),
    i
  );
}
function qe(e) {
  return (e = e.childContextTypes), e != null;
}
function Lo() {
  re(Ge), re(Fe);
}
function Af(e, t, n) {
  if (Fe.current !== zn) throw Error(M(168));
  ee(Fe, t), ee(Ge, n);
}
function ng(e, t, n) {
  var r = e.stateNode;
  if (((t = t.childContextTypes), typeof r.getChildContext != "function"))
    return n;
  r = r.getChildContext();
  for (var i in r) if (!(i in t)) throw Error(M(108, D1(e) || "Unknown", i));
  return ce({}, n, r);
}
function Oo(e) {
  return (
    (e =
      ((e = e.stateNode) && e.__reactInternalMemoizedMergedChildContext) || zn),
    (dr = Fe.current),
    ee(Fe, e),
    ee(Ge, Ge.current),
    !0
  );
}
function Rf(e, t, n) {
  var r = e.stateNode;
  if (!r) throw Error(M(169));
  n
    ? ((e = ng(e, t, dr)),
      (r.__reactInternalMemoizedMergedChildContext = e),
      re(Ge),
      re(Fe),
      ee(Fe, e))
    : re(Ge),
    ee(Ge, n);
}
var Gt = null,
  da = !1,
  sl = !1;
function rg(e) {
  Gt === null ? (Gt = [e]) : Gt.push(e);
}
function Qx(e) {
  (da = !0), rg(e);
}
function Hn() {
  if (!sl && Gt !== null) {
    sl = !0;
    var e = 0,
      t = X;
    try {
      var n = Gt;
      for (X = 1; e < n.length; e++) {
        var r = n[e];
        do r = r(!0);
        while (r !== null);
      }
      (Gt = null), (da = !1);
    } catch (i) {
      throw (Gt !== null && (Gt = Gt.slice(e + 1)), Rm(lc, Hn), i);
    } finally {
      (X = t), (sl = !1);
    }
  }
  return null;
}
var Mr = [],
  Dr = 0,
  jo = null,
  Io = 0,
  ft = [],
  ht = 0,
  fr = null,
  qt = 1,
  Xt = "";
function qn(e, t) {
  (Mr[Dr++] = Io), (Mr[Dr++] = jo), (jo = e), (Io = t);
}
function ig(e, t, n) {
  (ft[ht++] = qt), (ft[ht++] = Xt), (ft[ht++] = fr), (fr = e);
  var r = qt;
  e = Xt;
  var i = 32 - kt(r) - 1;
  (r &= ~(1 << i)), (n += 1);
  var s = 32 - kt(t) + i;
  if (30 < s) {
    var o = i - (i % 5);
    (s = (r & ((1 << o) - 1)).toString(32)),
      (r >>= o),
      (i -= o),
      (qt = (1 << (32 - kt(t) + i)) | (n << i) | r),
      (Xt = s + e);
  } else (qt = (1 << s) | (n << i) | r), (Xt = e);
}
function yc(e) {
  e.return !== null && (qn(e, 1), ig(e, 1, 0));
}
function vc(e) {
  for (; e === jo; )
    (jo = Mr[--Dr]), (Mr[Dr] = null), (Io = Mr[--Dr]), (Mr[Dr] = null);
  for (; e === fr; )
    (fr = ft[--ht]),
      (ft[ht] = null),
      (Xt = ft[--ht]),
      (ft[ht] = null),
      (qt = ft[--ht]),
      (ft[ht] = null);
}
var nt = null,
  tt = null,
  ie = !1,
  Tt = null;
function sg(e, t) {
  var n = pt(5, null, null, 0);
  (n.elementType = "DELETED"),
    (n.stateNode = t),
    (n.return = e),
    (t = e.deletions),
    t === null ? ((e.deletions = [n]), (e.flags |= 16)) : t.push(n);
}
function Mf(e, t) {
  switch (e.tag) {
    case 5:
      var n = e.type;
      return (
        (t =
          t.nodeType !== 1 || n.toLowerCase() !== t.nodeName.toLowerCase()
            ? null
            : t),
        t !== null
          ? ((e.stateNode = t), (nt = e), (tt = bn(t.firstChild)), !0)
          : !1
      );
    case 6:
      return (
        (t = e.pendingProps === "" || t.nodeType !== 3 ? null : t),
        t !== null ? ((e.stateNode = t), (nt = e), (tt = null), !0) : !1
      );
    case 13:
      return (
        (t = t.nodeType !== 8 ? null : t),
        t !== null
          ? ((n = fr !== null ? { id: qt, overflow: Xt } : null),
            (e.memoizedState = {
              dehydrated: t,
              treeContext: n,
              retryLane: 1073741824,
            }),
            (n = pt(18, null, null, 0)),
            (n.stateNode = t),
            (n.return = e),
            (e.child = n),
            (nt = e),
            (tt = null),
            !0)
          : !1
      );
    default:
      return !1;
  }
}
function ou(e) {
  return (e.mode & 1) !== 0 && (e.flags & 128) === 0;
}
function au(e) {
  if (ie) {
    var t = tt;
    if (t) {
      var n = t;
      if (!Mf(e, t)) {
        if (ou(e)) throw Error(M(418));
        t = bn(n.nextSibling);
        var r = nt;
        t && Mf(e, t)
          ? sg(r, n)
          : ((e.flags = (e.flags & -4097) | 2), (ie = !1), (nt = e));
      }
    } else {
      if (ou(e)) throw Error(M(418));
      (e.flags = (e.flags & -4097) | 2), (ie = !1), (nt = e);
    }
  }
}
function Df(e) {
  for (e = e.return; e !== null && e.tag !== 5 && e.tag !== 3 && e.tag !== 13; )
    e = e.return;
  nt = e;
}
function Gs(e) {
  if (e !== nt) return !1;
  if (!ie) return Df(e), (ie = !0), !1;
  var t;
  if (
    ((t = e.tag !== 3) &&
      !(t = e.tag !== 5) &&
      ((t = e.type),
      (t = t !== "head" && t !== "body" && !nu(e.type, e.memoizedProps))),
    t && (t = tt))
  ) {
    if (ou(e)) throw (og(), Error(M(418)));
    for (; t; ) sg(e, t), (t = bn(t.nextSibling));
  }
  if ((Df(e), e.tag === 13)) {
    if (((e = e.memoizedState), (e = e !== null ? e.dehydrated : null), !e))
      throw Error(M(317));
    e: {
      for (e = e.nextSibling, t = 0; e; ) {
        if (e.nodeType === 8) {
          var n = e.data;
          if (n === "/$") {
            if (t === 0) {
              tt = bn(e.nextSibling);
              break e;
            }
            t--;
          } else (n !== "$" && n !== "$!" && n !== "$?") || t++;
        }
        e = e.nextSibling;
      }
      tt = null;
    }
  } else tt = nt ? bn(e.stateNode.nextSibling) : null;
  return !0;
}
function og() {
  for (var e = tt; e; ) e = bn(e.nextSibling);
}
function ri() {
  (tt = nt = null), (ie = !1);
}
function xc(e) {
  Tt === null ? (Tt = [e]) : Tt.push(e);
}
var Gx = ln.ReactCurrentBatchConfig;
function Ci(e, t, n) {
  if (
    ((e = n.ref), e !== null && typeof e != "function" && typeof e != "object")
  ) {
    if (n._owner) {
      if (((n = n._owner), n)) {
        if (n.tag !== 1) throw Error(M(309));
        var r = n.stateNode;
      }
      if (!r) throw Error(M(147, e));
      var i = r,
        s = "" + e;
      return t !== null &&
        t.ref !== null &&
        typeof t.ref == "function" &&
        t.ref._stringRef === s
        ? t.ref
        : ((t = function (o) {
            var a = i.refs;
            o === null ? delete a[s] : (a[s] = o);
          }),
          (t._stringRef = s),
          t);
    }
    if (typeof e != "string") throw Error(M(284));
    if (!n._owner) throw Error(M(290, e));
  }
  return e;
}
function qs(e, t) {
  throw (
    ((e = Object.prototype.toString.call(t)),
    Error(
      M(
        31,
        e === "[object Object]"
          ? "object with keys {" + Object.keys(t).join(", ") + "}"
          : e
      )
    ))
  );
}
function Nf(e) {
  var t = e._init;
  return t(e._payload);
}
function ag(e) {
  function t(h, p) {
    if (e) {
      var g = h.deletions;
      g === null ? ((h.deletions = [p]), (h.flags |= 16)) : g.push(p);
    }
  }
  function n(h, p) {
    if (!e) return null;
    for (; p !== null; ) t(h, p), (p = p.sibling);
    return null;
  }
  function r(h, p) {
    for (h = new Map(); p !== null; )
      p.key !== null ? h.set(p.key, p) : h.set(p.index, p), (p = p.sibling);
    return h;
  }
  function i(h, p) {
    return (h = In(h, p)), (h.index = 0), (h.sibling = null), h;
  }
  function s(h, p, g) {
    return (
      (h.index = g),
      e
        ? ((g = h.alternate),
          g !== null
            ? ((g = g.index), g < p ? ((h.flags |= 2), p) : g)
            : ((h.flags |= 2), p))
        : ((h.flags |= 1048576), p)
    );
  }
  function o(h) {
    return e && h.alternate === null && (h.flags |= 2), h;
  }
  function a(h, p, g, S) {
    return p === null || p.tag !== 6
      ? ((p = fl(g, h.mode, S)), (p.return = h), p)
      : ((p = i(p, g)), (p.return = h), p);
  }
  function l(h, p, g, S) {
    var C = g.type;
    return C === Cr
      ? c(h, p, g.props.children, S, g.key)
      : p !== null &&
        (p.elementType === C ||
          (typeof C == "object" &&
            C !== null &&
            C.$$typeof === vn &&
            Nf(C) === p.type))
      ? ((S = i(p, g.props)), (S.ref = Ci(h, p, g)), (S.return = h), S)
      : ((S = vo(g.type, g.key, g.props, null, h.mode, S)),
        (S.ref = Ci(h, p, g)),
        (S.return = h),
        S);
  }
  function u(h, p, g, S) {
    return p === null ||
      p.tag !== 4 ||
      p.stateNode.containerInfo !== g.containerInfo ||
      p.stateNode.implementation !== g.implementation
      ? ((p = hl(g, h.mode, S)), (p.return = h), p)
      : ((p = i(p, g.children || [])), (p.return = h), p);
  }
  function c(h, p, g, S, C) {
    return p === null || p.tag !== 7
      ? ((p = ur(g, h.mode, S, C)), (p.return = h), p)
      : ((p = i(p, g)), (p.return = h), p);
  }
  function d(h, p, g) {
    if ((typeof p == "string" && p !== "") || typeof p == "number")
      return (p = fl("" + p, h.mode, g)), (p.return = h), p;
    if (typeof p == "object" && p !== null) {
      switch (p.$$typeof) {
        case _s:
          return (
            (g = vo(p.type, p.key, p.props, null, h.mode, g)),
            (g.ref = Ci(h, null, p)),
            (g.return = h),
            g
          );
        case Pr:
          return (p = hl(p, h.mode, g)), (p.return = h), p;
        case vn:
          var S = p._init;
          return d(h, S(p._payload), g);
      }
      if (Di(p) || vi(p))
        return (p = ur(p, h.mode, g, null)), (p.return = h), p;
      qs(h, p);
    }
    return null;
  }
  function f(h, p, g, S) {
    var C = p !== null ? p.key : null;
    if ((typeof g == "string" && g !== "") || typeof g == "number")
      return C !== null ? null : a(h, p, "" + g, S);
    if (typeof g == "object" && g !== null) {
      switch (g.$$typeof) {
        case _s:
          return g.key === C ? l(h, p, g, S) : null;
        case Pr:
          return g.key === C ? u(h, p, g, S) : null;
        case vn:
          return (C = g._init), f(h, p, C(g._payload), S);
      }
      if (Di(g) || vi(g)) return C !== null ? null : c(h, p, g, S, null);
      qs(h, g);
    }
    return null;
  }
  function v(h, p, g, S, C) {
    if ((typeof S == "string" && S !== "") || typeof S == "number")
      return (h = h.get(g) || null), a(p, h, "" + S, C);
    if (typeof S == "object" && S !== null) {
      switch (S.$$typeof) {
        case _s:
          return (h = h.get(S.key === null ? g : S.key) || null), l(p, h, S, C);
        case Pr:
          return (h = h.get(S.key === null ? g : S.key) || null), u(p, h, S, C);
        case vn:
          var k = S._init;
          return v(h, p, g, k(S._payload), C);
      }
      if (Di(S) || vi(S)) return (h = h.get(g) || null), c(p, h, S, C, null);
      qs(p, S);
    }
    return null;
  }
  function y(h, p, g, S) {
    for (
      var C = null, k = null, T = p, E = (p = 0), D = null;
      T !== null && E < g.length;
      E++
    ) {
      T.index > E ? ((D = T), (T = null)) : (D = T.sibling);
      var N = f(h, T, g[E], S);
      if (N === null) {
        T === null && (T = D);
        break;
      }
      e && T && N.alternate === null && t(h, T),
        (p = s(N, p, E)),
        k === null ? (C = N) : (k.sibling = N),
        (k = N),
        (T = D);
    }
    if (E === g.length) return n(h, T), ie && qn(h, E), C;
    if (T === null) {
      for (; E < g.length; E++)
        (T = d(h, g[E], S)),
          T !== null &&
            ((p = s(T, p, E)), k === null ? (C = T) : (k.sibling = T), (k = T));
      return ie && qn(h, E), C;
    }
    for (T = r(h, T); E < g.length; E++)
      (D = v(T, h, E, g[E], S)),
        D !== null &&
          (e && D.alternate !== null && T.delete(D.key === null ? E : D.key),
          (p = s(D, p, E)),
          k === null ? (C = D) : (k.sibling = D),
          (k = D));
    return (
      e &&
        T.forEach(function (j) {
          return t(h, j);
        }),
      ie && qn(h, E),
      C
    );
  }
  function m(h, p, g, S) {
    var C = vi(g);
    if (typeof C != "function") throw Error(M(150));
    if (((g = C.call(g)), g == null)) throw Error(M(151));
    for (
      var k = (C = null), T = p, E = (p = 0), D = null, N = g.next();
      T !== null && !N.done;
      E++, N = g.next()
    ) {
      T.index > E ? ((D = T), (T = null)) : (D = T.sibling);
      var j = f(h, T, N.value, S);
      if (j === null) {
        T === null && (T = D);
        break;
      }
      e && T && j.alternate === null && t(h, T),
        (p = s(j, p, E)),
        k === null ? (C = j) : (k.sibling = j),
        (k = j),
        (T = D);
    }
    if (N.done) return n(h, T), ie && qn(h, E), C;
    if (T === null) {
      for (; !N.done; E++, N = g.next())
        (N = d(h, N.value, S)),
          N !== null &&
            ((p = s(N, p, E)), k === null ? (C = N) : (k.sibling = N), (k = N));
      return ie && qn(h, E), C;
    }
    for (T = r(h, T); !N.done; E++, N = g.next())
      (N = v(T, h, E, N.value, S)),
        N !== null &&
          (e && N.alternate !== null && T.delete(N.key === null ? E : N.key),
          (p = s(N, p, E)),
          k === null ? (C = N) : (k.sibling = N),
          (k = N));
    return (
      e &&
        T.forEach(function (I) {
          return t(h, I);
        }),
      ie && qn(h, E),
      C
    );
  }
  function x(h, p, g, S) {
    if (
      (typeof g == "object" &&
        g !== null &&
        g.type === Cr &&
        g.key === null &&
        (g = g.props.children),
      typeof g == "object" && g !== null)
    ) {
      switch (g.$$typeof) {
        case _s:
          e: {
            for (var C = g.key, k = p; k !== null; ) {
              if (k.key === C) {
                if (((C = g.type), C === Cr)) {
                  if (k.tag === 7) {
                    n(h, k.sibling),
                      (p = i(k, g.props.children)),
                      (p.return = h),
                      (h = p);
                    break e;
                  }
                } else if (
                  k.elementType === C ||
                  (typeof C == "object" &&
                    C !== null &&
                    C.$$typeof === vn &&
                    Nf(C) === k.type)
                ) {
                  n(h, k.sibling),
                    (p = i(k, g.props)),
                    (p.ref = Ci(h, k, g)),
                    (p.return = h),
                    (h = p);
                  break e;
                }
                n(h, k);
                break;
              } else t(h, k);
              k = k.sibling;
            }
            g.type === Cr
              ? ((p = ur(g.props.children, h.mode, S, g.key)),
                (p.return = h),
                (h = p))
              : ((S = vo(g.type, g.key, g.props, null, h.mode, S)),
                (S.ref = Ci(h, p, g)),
                (S.return = h),
                (h = S));
          }
          return o(h);
        case Pr:
          e: {
            for (k = g.key; p !== null; ) {
              if (p.key === k)
                if (
                  p.tag === 4 &&
                  p.stateNode.containerInfo === g.containerInfo &&
                  p.stateNode.implementation === g.implementation
                ) {
                  n(h, p.sibling),
                    (p = i(p, g.children || [])),
                    (p.return = h),
                    (h = p);
                  break e;
                } else {
                  n(h, p);
                  break;
                }
              else t(h, p);
              p = p.sibling;
            }
            (p = hl(g, h.mode, S)), (p.return = h), (h = p);
          }
          return o(h);
        case vn:
          return (k = g._init), x(h, p, k(g._payload), S);
      }
      if (Di(g)) return y(h, p, g, S);
      if (vi(g)) return m(h, p, g, S);
      qs(h, g);
    }
    return (typeof g == "string" && g !== "") || typeof g == "number"
      ? ((g = "" + g),
        p !== null && p.tag === 6
          ? (n(h, p.sibling), (p = i(p, g)), (p.return = h), (h = p))
          : (n(h, p), (p = fl(g, h.mode, S)), (p.return = h), (h = p)),
        o(h))
      : n(h, p);
  }
  return x;
}
var ii = ag(!0),
  lg = ag(!1),
  Fo = Wn(null),
  _o = null,
  Nr = null,
  wc = null;
function Sc() {
  wc = Nr = _o = null;
}
function Pc(e) {
  var t = Fo.current;
  re(Fo), (e._currentValue = t);
}
function lu(e, t, n) {
  for (; e !== null; ) {
    var r = e.alternate;
    if (
      ((e.childLanes & t) !== t
        ? ((e.childLanes |= t), r !== null && (r.childLanes |= t))
        : r !== null && (r.childLanes & t) !== t && (r.childLanes |= t),
      e === n)
    )
      break;
    e = e.return;
  }
}
function $r(e, t) {
  (_o = e),
    (wc = Nr = null),
    (e = e.dependencies),
    e !== null &&
      e.firstContext !== null &&
      (e.lanes & t && (Qe = !0), (e.firstContext = null));
}
function gt(e) {
  var t = e._currentValue;
  if (wc !== e)
    if (((e = { context: e, memoizedValue: t, next: null }), Nr === null)) {
      if (_o === null) throw Error(M(308));
      (Nr = e), (_o.dependencies = { lanes: 0, firstContext: e });
    } else Nr = Nr.next = e;
  return t;
}
var er = null;
function Cc(e) {
  er === null ? (er = [e]) : er.push(e);
}
function ug(e, t, n, r) {
  var i = t.interleaved;
  return (
    i === null ? ((n.next = n), Cc(t)) : ((n.next = i.next), (i.next = n)),
    (t.interleaved = n),
    rn(e, r)
  );
}
function rn(e, t) {
  e.lanes |= t;
  var n = e.alternate;
  for (n !== null && (n.lanes |= t), n = e, e = e.return; e !== null; )
    (e.childLanes |= t),
      (n = e.alternate),
      n !== null && (n.childLanes |= t),
      (n = e),
      (e = e.return);
  return n.tag === 3 ? n.stateNode : null;
}
var xn = !1;
function Ec(e) {
  e.updateQueue = {
    baseState: e.memoizedState,
    firstBaseUpdate: null,
    lastBaseUpdate: null,
    shared: { pending: null, interleaved: null, lanes: 0 },
    effects: null,
  };
}
function cg(e, t) {
  (e = e.updateQueue),
    t.updateQueue === e &&
      (t.updateQueue = {
        baseState: e.baseState,
        firstBaseUpdate: e.firstBaseUpdate,
        lastBaseUpdate: e.lastBaseUpdate,
        shared: e.shared,
        effects: e.effects,
      });
}
function Zt(e, t) {
  return {
    eventTime: e,
    lane: t,
    tag: 0,
    payload: null,
    callback: null,
    next: null,
  };
}
function Ln(e, t, n) {
  var r = e.updateQueue;
  if (r === null) return null;
  if (((r = r.shared), K & 2)) {
    var i = r.pending;
    return (
      i === null ? (t.next = t) : ((t.next = i.next), (i.next = t)),
      (r.pending = t),
      rn(e, n)
    );
  }
  return (
    (i = r.interleaved),
    i === null ? ((t.next = t), Cc(r)) : ((t.next = i.next), (i.next = t)),
    (r.interleaved = t),
    rn(e, n)
  );
}
function fo(e, t, n) {
  if (
    ((t = t.updateQueue), t !== null && ((t = t.shared), (n & 4194240) !== 0))
  ) {
    var r = t.lanes;
    (r &= e.pendingLanes), (n |= r), (t.lanes = n), uc(e, n);
  }
}
function bf(e, t) {
  var n = e.updateQueue,
    r = e.alternate;
  if (r !== null && ((r = r.updateQueue), n === r)) {
    var i = null,
      s = null;
    if (((n = n.firstBaseUpdate), n !== null)) {
      do {
        var o = {
          eventTime: n.eventTime,
          lane: n.lane,
          tag: n.tag,
          payload: n.payload,
          callback: n.callback,
          next: null,
        };
        s === null ? (i = s = o) : (s = s.next = o), (n = n.next);
      } while (n !== null);
      s === null ? (i = s = t) : (s = s.next = t);
    } else i = s = t;
    (n = {
      baseState: r.baseState,
      firstBaseUpdate: i,
      lastBaseUpdate: s,
      shared: r.shared,
      effects: r.effects,
    }),
      (e.updateQueue = n);
    return;
  }
  (e = n.lastBaseUpdate),
    e === null ? (n.firstBaseUpdate = t) : (e.next = t),
    (n.lastBaseUpdate = t);
}
function Vo(e, t, n, r) {
  var i = e.updateQueue;
  xn = !1;
  var s = i.firstBaseUpdate,
    o = i.lastBaseUpdate,
    a = i.shared.pending;
  if (a !== null) {
    i.shared.pending = null;
    var l = a,
      u = l.next;
    (l.next = null), o === null ? (s = u) : (o.next = u), (o = l);
    var c = e.alternate;
    c !== null &&
      ((c = c.updateQueue),
      (a = c.lastBaseUpdate),
      a !== o &&
        (a === null ? (c.firstBaseUpdate = u) : (a.next = u),
        (c.lastBaseUpdate = l)));
  }
  if (s !== null) {
    var d = i.baseState;
    (o = 0), (c = u = l = null), (a = s);
    do {
      var f = a.lane,
        v = a.eventTime;
      if ((r & f) === f) {
        c !== null &&
          (c = c.next =
            {
              eventTime: v,
              lane: 0,
              tag: a.tag,
              payload: a.payload,
              callback: a.callback,
              next: null,
            });
        e: {
          var y = e,
            m = a;
          switch (((f = t), (v = n), m.tag)) {
            case 1:
              if (((y = m.payload), typeof y == "function")) {
                d = y.call(v, d, f);
                break e;
              }
              d = y;
              break e;
            case 3:
              y.flags = (y.flags & -65537) | 128;
            case 0:
              if (
                ((y = m.payload),
                (f = typeof y == "function" ? y.call(v, d, f) : y),
                f == null)
              )
                break e;
              d = ce({}, d, f);
              break e;
            case 2:
              xn = !0;
          }
        }
        a.callback !== null &&
          a.lane !== 0 &&
          ((e.flags |= 64),
          (f = i.effects),
          f === null ? (i.effects = [a]) : f.push(a));
      } else
        (v = {
          eventTime: v,
          lane: f,
          tag: a.tag,
          payload: a.payload,
          callback: a.callback,
          next: null,
        }),
          c === null ? ((u = c = v), (l = d)) : (c = c.next = v),
          (o |= f);
      if (((a = a.next), a === null)) {
        if (((a = i.shared.pending), a === null)) break;
        (f = a),
          (a = f.next),
          (f.next = null),
          (i.lastBaseUpdate = f),
          (i.shared.pending = null);
      }
    } while (!0);
    if (
      (c === null && (l = d),
      (i.baseState = l),
      (i.firstBaseUpdate = u),
      (i.lastBaseUpdate = c),
      (t = i.shared.interleaved),
      t !== null)
    ) {
      i = t;
      do (o |= i.lane), (i = i.next);
      while (i !== t);
    } else s === null && (i.shared.lanes = 0);
    (pr |= o), (e.lanes = o), (e.memoizedState = d);
  }
}
function Lf(e, t, n) {
  if (((e = t.effects), (t.effects = null), e !== null))
    for (t = 0; t < e.length; t++) {
      var r = e[t],
        i = r.callback;
      if (i !== null) {
        if (((r.callback = null), (r = n), typeof i != "function"))
          throw Error(M(191, i));
        i.call(r);
      }
    }
}
var Ms = {},
  _t = Wn(Ms),
  as = Wn(Ms),
  ls = Wn(Ms);
function tr(e) {
  if (e === Ms) throw Error(M(174));
  return e;
}
function Tc(e, t) {
  switch ((ee(ls, t), ee(as, e), ee(_t, Ms), (e = t.nodeType), e)) {
    case 9:
    case 11:
      t = (t = t.documentElement) ? t.namespaceURI : Ul(null, "");
      break;
    default:
      (e = e === 8 ? t.parentNode : t),
        (t = e.namespaceURI || null),
        (e = e.tagName),
        (t = Ul(t, e));
  }
  re(_t), ee(_t, t);
}
function si() {
  re(_t), re(as), re(ls);
}
function dg(e) {
  tr(ls.current);
  var t = tr(_t.current),
    n = Ul(t, e.type);
  t !== n && (ee(as, e), ee(_t, n));
}
function kc(e) {
  as.current === e && (re(_t), re(as));
}
var oe = Wn(0);
function zo(e) {
  for (var t = e; t !== null; ) {
    if (t.tag === 13) {
      var n = t.memoizedState;
      if (
        n !== null &&
        ((n = n.dehydrated), n === null || n.data === "$?" || n.data === "$!")
      )
        return t;
    } else if (t.tag === 19 && t.memoizedProps.revealOrder !== void 0) {
      if (t.flags & 128) return t;
    } else if (t.child !== null) {
      (t.child.return = t), (t = t.child);
      continue;
    }
    if (t === e) break;
    for (; t.sibling === null; ) {
      if (t.return === null || t.return === e) return null;
      t = t.return;
    }
    (t.sibling.return = t.return), (t = t.sibling);
  }
  return null;
}
var ol = [];
function Ac() {
  for (var e = 0; e < ol.length; e++)
    ol[e]._workInProgressVersionPrimary = null;
  ol.length = 0;
}
var ho = ln.ReactCurrentDispatcher,
  al = ln.ReactCurrentBatchConfig,
  hr = 0,
  ue = null,
  we = null,
  Ce = null,
  Bo = !1,
  Bi = !1,
  us = 0,
  qx = 0;
function De() {
  throw Error(M(321));
}
function Rc(e, t) {
  if (t === null) return !1;
  for (var n = 0; n < t.length && n < e.length; n++)
    if (!Mt(e[n], t[n])) return !1;
  return !0;
}
function Mc(e, t, n, r, i, s) {
  if (
    ((hr = s),
    (ue = t),
    (t.memoizedState = null),
    (t.updateQueue = null),
    (t.lanes = 0),
    (ho.current = e === null || e.memoizedState === null ? Jx : ew),
    (e = n(r, i)),
    Bi)
  ) {
    s = 0;
    do {
      if (((Bi = !1), (us = 0), 25 <= s)) throw Error(M(301));
      (s += 1),
        (Ce = we = null),
        (t.updateQueue = null),
        (ho.current = tw),
        (e = n(r, i));
    } while (Bi);
  }
  if (
    ((ho.current = Uo),
    (t = we !== null && we.next !== null),
    (hr = 0),
    (Ce = we = ue = null),
    (Bo = !1),
    t)
  )
    throw Error(M(300));
  return e;
}
function Dc() {
  var e = us !== 0;
  return (us = 0), e;
}
function bt() {
  var e = {
    memoizedState: null,
    baseState: null,
    baseQueue: null,
    queue: null,
    next: null,
  };
  return Ce === null ? (ue.memoizedState = Ce = e) : (Ce = Ce.next = e), Ce;
}
function yt() {
  if (we === null) {
    var e = ue.alternate;
    e = e !== null ? e.memoizedState : null;
  } else e = we.next;
  var t = Ce === null ? ue.memoizedState : Ce.next;
  if (t !== null) (Ce = t), (we = e);
  else {
    if (e === null) throw Error(M(310));
    (we = e),
      (e = {
        memoizedState: we.memoizedState,
        baseState: we.baseState,
        baseQueue: we.baseQueue,
        queue: we.queue,
        next: null,
      }),
      Ce === null ? (ue.memoizedState = Ce = e) : (Ce = Ce.next = e);
  }
  return Ce;
}
function cs(e, t) {
  return typeof t == "function" ? t(e) : t;
}
function ll(e) {
  var t = yt(),
    n = t.queue;
  if (n === null) throw Error(M(311));
  n.lastRenderedReducer = e;
  var r = we,
    i = r.baseQueue,
    s = n.pending;
  if (s !== null) {
    if (i !== null) {
      var o = i.next;
      (i.next = s.next), (s.next = o);
    }
    (r.baseQueue = i = s), (n.pending = null);
  }
  if (i !== null) {
    (s = i.next), (r = r.baseState);
    var a = (o = null),
      l = null,
      u = s;
    do {
      var c = u.lane;
      if ((hr & c) === c)
        l !== null &&
          (l = l.next =
            {
              lane: 0,
              action: u.action,
              hasEagerState: u.hasEagerState,
              eagerState: u.eagerState,
              next: null,
            }),
          (r = u.hasEagerState ? u.eagerState : e(r, u.action));
      else {
        var d = {
          lane: c,
          action: u.action,
          hasEagerState: u.hasEagerState,
          eagerState: u.eagerState,
          next: null,
        };
        l === null ? ((a = l = d), (o = r)) : (l = l.next = d),
          (ue.lanes |= c),
          (pr |= c);
      }
      u = u.next;
    } while (u !== null && u !== s);
    l === null ? (o = r) : (l.next = a),
      Mt(r, t.memoizedState) || (Qe = !0),
      (t.memoizedState = r),
      (t.baseState = o),
      (t.baseQueue = l),
      (n.lastRenderedState = r);
  }
  if (((e = n.interleaved), e !== null)) {
    i = e;
    do (s = i.lane), (ue.lanes |= s), (pr |= s), (i = i.next);
    while (i !== e);
  } else i === null && (n.lanes = 0);
  return [t.memoizedState, n.dispatch];
}
function ul(e) {
  var t = yt(),
    n = t.queue;
  if (n === null) throw Error(M(311));
  n.lastRenderedReducer = e;
  var r = n.dispatch,
    i = n.pending,
    s = t.memoizedState;
  if (i !== null) {
    n.pending = null;
    var o = (i = i.next);
    do (s = e(s, o.action)), (o = o.next);
    while (o !== i);
    Mt(s, t.memoizedState) || (Qe = !0),
      (t.memoizedState = s),
      t.baseQueue === null && (t.baseState = s),
      (n.lastRenderedState = s);
  }
  return [s, r];
}
function fg() {}
function hg(e, t) {
  var n = ue,
    r = yt(),
    i = t(),
    s = !Mt(r.memoizedState, i);
  if (
    (s && ((r.memoizedState = i), (Qe = !0)),
    (r = r.queue),
    Nc(gg.bind(null, n, r, e), [e]),
    r.getSnapshot !== t || s || (Ce !== null && Ce.memoizedState.tag & 1))
  ) {
    if (
      ((n.flags |= 2048),
      ds(9, mg.bind(null, n, r, i, t), void 0, null),
      Ee === null)
    )
      throw Error(M(349));
    hr & 30 || pg(n, t, i);
  }
  return i;
}
function pg(e, t, n) {
  (e.flags |= 16384),
    (e = { getSnapshot: t, value: n }),
    (t = ue.updateQueue),
    t === null
      ? ((t = { lastEffect: null, stores: null }),
        (ue.updateQueue = t),
        (t.stores = [e]))
      : ((n = t.stores), n === null ? (t.stores = [e]) : n.push(e));
}
function mg(e, t, n, r) {
  (t.value = n), (t.getSnapshot = r), yg(t) && vg(e);
}
function gg(e, t, n) {
  return n(function () {
    yg(t) && vg(e);
  });
}
function yg(e) {
  var t = e.getSnapshot;
  e = e.value;
  try {
    var n = t();
    return !Mt(e, n);
  } catch {
    return !0;
  }
}
function vg(e) {
  var t = rn(e, 1);
  t !== null && At(t, e, 1, -1);
}
function Of(e) {
  var t = bt();
  return (
    typeof e == "function" && (e = e()),
    (t.memoizedState = t.baseState = e),
    (e = {
      pending: null,
      interleaved: null,
      lanes: 0,
      dispatch: null,
      lastRenderedReducer: cs,
      lastRenderedState: e,
    }),
    (t.queue = e),
    (e = e.dispatch = Zx.bind(null, ue, e)),
    [t.memoizedState, e]
  );
}
function ds(e, t, n, r) {
  return (
    (e = { tag: e, create: t, destroy: n, deps: r, next: null }),
    (t = ue.updateQueue),
    t === null
      ? ((t = { lastEffect: null, stores: null }),
        (ue.updateQueue = t),
        (t.lastEffect = e.next = e))
      : ((n = t.lastEffect),
        n === null
          ? (t.lastEffect = e.next = e)
          : ((r = n.next), (n.next = e), (e.next = r), (t.lastEffect = e))),
    e
  );
}
function xg() {
  return yt().memoizedState;
}
function po(e, t, n, r) {
  var i = bt();
  (ue.flags |= e),
    (i.memoizedState = ds(1 | t, n, void 0, r === void 0 ? null : r));
}
function fa(e, t, n, r) {
  var i = yt();
  r = r === void 0 ? null : r;
  var s = void 0;
  if (we !== null) {
    var o = we.memoizedState;
    if (((s = o.destroy), r !== null && Rc(r, o.deps))) {
      i.memoizedState = ds(t, n, s, r);
      return;
    }
  }
  (ue.flags |= e), (i.memoizedState = ds(1 | t, n, s, r));
}
function jf(e, t) {
  return po(8390656, 8, e, t);
}
function Nc(e, t) {
  return fa(2048, 8, e, t);
}
function wg(e, t) {
  return fa(4, 2, e, t);
}
function Sg(e, t) {
  return fa(4, 4, e, t);
}
function Pg(e, t) {
  if (typeof t == "function")
    return (
      (e = e()),
      t(e),
      function () {
        t(null);
      }
    );
  if (t != null)
    return (
      (e = e()),
      (t.current = e),
      function () {
        t.current = null;
      }
    );
}
function Cg(e, t, n) {
  return (
    (n = n != null ? n.concat([e]) : null), fa(4, 4, Pg.bind(null, t, e), n)
  );
}
function bc() {}
function Eg(e, t) {
  var n = yt();
  t = t === void 0 ? null : t;
  var r = n.memoizedState;
  return r !== null && t !== null && Rc(t, r[1])
    ? r[0]
    : ((n.memoizedState = [e, t]), e);
}
function Tg(e, t) {
  var n = yt();
  t = t === void 0 ? null : t;
  var r = n.memoizedState;
  return r !== null && t !== null && Rc(t, r[1])
    ? r[0]
    : ((e = e()), (n.memoizedState = [e, t]), e);
}
function kg(e, t, n) {
  return hr & 21
    ? (Mt(n, t) || ((n = Nm()), (ue.lanes |= n), (pr |= n), (e.baseState = !0)),
      t)
    : (e.baseState && ((e.baseState = !1), (Qe = !0)), (e.memoizedState = n));
}
function Xx(e, t) {
  var n = X;
  (X = n !== 0 && 4 > n ? n : 4), e(!0);
  var r = al.transition;
  al.transition = {};
  try {
    e(!1), t();
  } finally {
    (X = n), (al.transition = r);
  }
}
function Ag() {
  return yt().memoizedState;
}
function Yx(e, t, n) {
  var r = jn(e);
  if (
    ((n = {
      lane: r,
      action: n,
      hasEagerState: !1,
      eagerState: null,
      next: null,
    }),
    Rg(e))
  )
    Mg(t, n);
  else if (((n = ug(e, t, n, r)), n !== null)) {
    var i = $e();
    At(n, e, r, i), Dg(n, t, r);
  }
}
function Zx(e, t, n) {
  var r = jn(e),
    i = { lane: r, action: n, hasEagerState: !1, eagerState: null, next: null };
  if (Rg(e)) Mg(t, i);
  else {
    var s = e.alternate;
    if (
      e.lanes === 0 &&
      (s === null || s.lanes === 0) &&
      ((s = t.lastRenderedReducer), s !== null)
    )
      try {
        var o = t.lastRenderedState,
          a = s(o, n);
        if (((i.hasEagerState = !0), (i.eagerState = a), Mt(a, o))) {
          var l = t.interleaved;
          l === null
            ? ((i.next = i), Cc(t))
            : ((i.next = l.next), (l.next = i)),
            (t.interleaved = i);
          return;
        }
      } catch {
      } finally {
      }
    (n = ug(e, t, i, r)),
      n !== null && ((i = $e()), At(n, e, r, i), Dg(n, t, r));
  }
}
function Rg(e) {
  var t = e.alternate;
  return e === ue || (t !== null && t === ue);
}
function Mg(e, t) {
  Bi = Bo = !0;
  var n = e.pending;
  n === null ? (t.next = t) : ((t.next = n.next), (n.next = t)),
    (e.pending = t);
}
function Dg(e, t, n) {
  if (n & 4194240) {
    var r = t.lanes;
    (r &= e.pendingLanes), (n |= r), (t.lanes = n), uc(e, n);
  }
}
var Uo = {
    readContext: gt,
    useCallback: De,
    useContext: De,
    useEffect: De,
    useImperativeHandle: De,
    useInsertionEffect: De,
    useLayoutEffect: De,
    useMemo: De,
    useReducer: De,
    useRef: De,
    useState: De,
    useDebugValue: De,
    useDeferredValue: De,
    useTransition: De,
    useMutableSource: De,
    useSyncExternalStore: De,
    useId: De,
    unstable_isNewReconciler: !1,
  },
  Jx = {
    readContext: gt,
    useCallback: function (e, t) {
      return (bt().memoizedState = [e, t === void 0 ? null : t]), e;
    },
    useContext: gt,
    useEffect: jf,
    useImperativeHandle: function (e, t, n) {
      return (
        (n = n != null ? n.concat([e]) : null),
        po(4194308, 4, Pg.bind(null, t, e), n)
      );
    },
    useLayoutEffect: function (e, t) {
      return po(4194308, 4, e, t);
    },
    useInsertionEffect: function (e, t) {
      return po(4, 2, e, t);
    },
    useMemo: function (e, t) {
      var n = bt();
      return (
        (t = t === void 0 ? null : t), (e = e()), (n.memoizedState = [e, t]), e
      );
    },
    useReducer: function (e, t, n) {
      var r = bt();
      return (
        (t = n !== void 0 ? n(t) : t),
        (r.memoizedState = r.baseState = t),
        (e = {
          pending: null,
          interleaved: null,
          lanes: 0,
          dispatch: null,
          lastRenderedReducer: e,
          lastRenderedState: t,
        }),
        (r.queue = e),
        (e = e.dispatch = Yx.bind(null, ue, e)),
        [r.memoizedState, e]
      );
    },
    useRef: function (e) {
      var t = bt();
      return (e = { current: e }), (t.memoizedState = e);
    },
    useState: Of,
    useDebugValue: bc,
    useDeferredValue: function (e) {
      return (bt().memoizedState = e);
    },
    useTransition: function () {
      var e = Of(!1),
        t = e[0];
      return (e = Xx.bind(null, e[1])), (bt().memoizedState = e), [t, e];
    },
    useMutableSource: function () {},
    useSyncExternalStore: function (e, t, n) {
      var r = ue,
        i = bt();
      if (ie) {
        if (n === void 0) throw Error(M(407));
        n = n();
      } else {
        if (((n = t()), Ee === null)) throw Error(M(349));
        hr & 30 || pg(r, t, n);
      }
      i.memoizedState = n;
      var s = { value: n, getSnapshot: t };
      return (
        (i.queue = s),
        jf(gg.bind(null, r, s, e), [e]),
        (r.flags |= 2048),
        ds(9, mg.bind(null, r, s, n, t), void 0, null),
        n
      );
    },
    useId: function () {
      var e = bt(),
        t = Ee.identifierPrefix;
      if (ie) {
        var n = Xt,
          r = qt;
        (n = (r & ~(1 << (32 - kt(r) - 1))).toString(32) + n),
          (t = ":" + t + "R" + n),
          (n = us++),
          0 < n && (t += "H" + n.toString(32)),
          (t += ":");
      } else (n = qx++), (t = ":" + t + "r" + n.toString(32) + ":");
      return (e.memoizedState = t);
    },
    unstable_isNewReconciler: !1,
  },
  ew = {
    readContext: gt,
    useCallback: Eg,
    useContext: gt,
    useEffect: Nc,
    useImperativeHandle: Cg,
    useInsertionEffect: wg,
    useLayoutEffect: Sg,
    useMemo: Tg,
    useReducer: ll,
    useRef: xg,
    useState: function () {
      return ll(cs);
    },
    useDebugValue: bc,
    useDeferredValue: function (e) {
      var t = yt();
      return kg(t, we.memoizedState, e);
    },
    useTransition: function () {
      var e = ll(cs)[0],
        t = yt().memoizedState;
      return [e, t];
    },
    useMutableSource: fg,
    useSyncExternalStore: hg,
    useId: Ag,
    unstable_isNewReconciler: !1,
  },
  tw = {
    readContext: gt,
    useCallback: Eg,
    useContext: gt,
    useEffect: Nc,
    useImperativeHandle: Cg,
    useInsertionEffect: wg,
    useLayoutEffect: Sg,
    useMemo: Tg,
    useReducer: ul,
    useRef: xg,
    useState: function () {
      return ul(cs);
    },
    useDebugValue: bc,
    useDeferredValue: function (e) {
      var t = yt();
      return we === null ? (t.memoizedState = e) : kg(t, we.memoizedState, e);
    },
    useTransition: function () {
      var e = ul(cs)[0],
        t = yt().memoizedState;
      return [e, t];
    },
    useMutableSource: fg,
    useSyncExternalStore: hg,
    useId: Ag,
    unstable_isNewReconciler: !1,
  };
function St(e, t) {
  if (e && e.defaultProps) {
    (t = ce({}, t)), (e = e.defaultProps);
    for (var n in e) t[n] === void 0 && (t[n] = e[n]);
    return t;
  }
  return t;
}
function uu(e, t, n, r) {
  (t = e.memoizedState),
    (n = n(r, t)),
    (n = n == null ? t : ce({}, t, n)),
    (e.memoizedState = n),
    e.lanes === 0 && (e.updateQueue.baseState = n);
}
var ha = {
  isMounted: function (e) {
    return (e = e._reactInternals) ? xr(e) === e : !1;
  },
  enqueueSetState: function (e, t, n) {
    e = e._reactInternals;
    var r = $e(),
      i = jn(e),
      s = Zt(r, i);
    (s.payload = t),
      n != null && (s.callback = n),
      (t = Ln(e, s, i)),
      t !== null && (At(t, e, i, r), fo(t, e, i));
  },
  enqueueReplaceState: function (e, t, n) {
    e = e._reactInternals;
    var r = $e(),
      i = jn(e),
      s = Zt(r, i);
    (s.tag = 1),
      (s.payload = t),
      n != null && (s.callback = n),
      (t = Ln(e, s, i)),
      t !== null && (At(t, e, i, r), fo(t, e, i));
  },
  enqueueForceUpdate: function (e, t) {
    e = e._reactInternals;
    var n = $e(),
      r = jn(e),
      i = Zt(n, r);
    (i.tag = 2),
      t != null && (i.callback = t),
      (t = Ln(e, i, r)),
      t !== null && (At(t, e, r, n), fo(t, e, r));
  },
};
function If(e, t, n, r, i, s, o) {
  return (
    (e = e.stateNode),
    typeof e.shouldComponentUpdate == "function"
      ? e.shouldComponentUpdate(r, s, o)
      : t.prototype && t.prototype.isPureReactComponent
      ? !rs(n, r) || !rs(i, s)
      : !0
  );
}
function Ng(e, t, n) {
  var r = !1,
    i = zn,
    s = t.contextType;
  return (
    typeof s == "object" && s !== null
      ? (s = gt(s))
      : ((i = qe(t) ? dr : Fe.current),
        (r = t.contextTypes),
        (s = (r = r != null) ? ni(e, i) : zn)),
    (t = new t(n, s)),
    (e.memoizedState = t.state !== null && t.state !== void 0 ? t.state : null),
    (t.updater = ha),
    (e.stateNode = t),
    (t._reactInternals = e),
    r &&
      ((e = e.stateNode),
      (e.__reactInternalMemoizedUnmaskedChildContext = i),
      (e.__reactInternalMemoizedMaskedChildContext = s)),
    t
  );
}
function Ff(e, t, n, r) {
  (e = t.state),
    typeof t.componentWillReceiveProps == "function" &&
      t.componentWillReceiveProps(n, r),
    typeof t.UNSAFE_componentWillReceiveProps == "function" &&
      t.UNSAFE_componentWillReceiveProps(n, r),
    t.state !== e && ha.enqueueReplaceState(t, t.state, null);
}
function cu(e, t, n, r) {
  var i = e.stateNode;
  (i.props = n), (i.state = e.memoizedState), (i.refs = {}), Ec(e);
  var s = t.contextType;
  typeof s == "object" && s !== null
    ? (i.context = gt(s))
    : ((s = qe(t) ? dr : Fe.current), (i.context = ni(e, s))),
    (i.state = e.memoizedState),
    (s = t.getDerivedStateFromProps),
    typeof s == "function" && (uu(e, t, s, n), (i.state = e.memoizedState)),
    typeof t.getDerivedStateFromProps == "function" ||
      typeof i.getSnapshotBeforeUpdate == "function" ||
      (typeof i.UNSAFE_componentWillMount != "function" &&
        typeof i.componentWillMount != "function") ||
      ((t = i.state),
      typeof i.componentWillMount == "function" && i.componentWillMount(),
      typeof i.UNSAFE_componentWillMount == "function" &&
        i.UNSAFE_componentWillMount(),
      t !== i.state && ha.enqueueReplaceState(i, i.state, null),
      Vo(e, n, i, r),
      (i.state = e.memoizedState)),
    typeof i.componentDidMount == "function" && (e.flags |= 4194308);
}
function oi(e, t) {
  try {
    var n = "",
      r = t;
    do (n += M1(r)), (r = r.return);
    while (r);
    var i = n;
  } catch (s) {
    i =
      `
  Error generating stack: ` +
      s.message +
      `
  ` +
      s.stack;
  }
  return { value: e, source: t, stack: i, digest: null };
}
function cl(e, t, n) {
  return { value: e, source: null, stack: n ?? null, digest: t ?? null };
}
function du(e, t) {
  try {
    console.error(t.value);
  } catch (n) {
    setTimeout(function () {
      throw n;
    });
  }
}
var nw = typeof WeakMap == "function" ? WeakMap : Map;
function bg(e, t, n) {
  (n = Zt(-1, n)), (n.tag = 3), (n.payload = { element: null });
  var r = t.value;
  return (
    (n.callback = function () {
      Wo || ((Wo = !0), (Su = r)), du(e, t);
    }),
    n
  );
}
function Lg(e, t, n) {
  (n = Zt(-1, n)), (n.tag = 3);
  var r = e.type.getDerivedStateFromError;
  if (typeof r == "function") {
    var i = t.value;
    (n.payload = function () {
      return r(i);
    }),
      (n.callback = function () {
        du(e, t);
      });
  }
  var s = e.stateNode;
  return (
    s !== null &&
      typeof s.componentDidCatch == "function" &&
      (n.callback = function () {
        du(e, t),
          typeof r != "function" &&
            (On === null ? (On = new Set([this])) : On.add(this));
        var o = t.stack;
        this.componentDidCatch(t.value, {
          componentStack: o !== null ? o : "",
        });
      }),
    n
  );
}
function _f(e, t, n) {
  var r = e.pingCache;
  if (r === null) {
    r = e.pingCache = new nw();
    var i = new Set();
    r.set(t, i);
  } else (i = r.get(t)), i === void 0 && ((i = new Set()), r.set(t, i));
  i.has(n) || (i.add(n), (e = gw.bind(null, e, t, n)), t.then(e, e));
}
function Vf(e) {
  do {
    var t;
    if (
      ((t = e.tag === 13) &&
        ((t = e.memoizedState), (t = t !== null ? t.dehydrated !== null : !0)),
      t)
    )
      return e;
    e = e.return;
  } while (e !== null);
  return null;
}
function zf(e, t, n, r, i) {
  return e.mode & 1
    ? ((e.flags |= 65536), (e.lanes = i), e)
    : (e === t
        ? (e.flags |= 65536)
        : ((e.flags |= 128),
          (n.flags |= 131072),
          (n.flags &= -52805),
          n.tag === 1 &&
            (n.alternate === null
              ? (n.tag = 17)
              : ((t = Zt(-1, 1)), (t.tag = 2), Ln(n, t, 1))),
          (n.lanes |= 1)),
      e);
}
var rw = ln.ReactCurrentOwner,
  Qe = !1;
function Be(e, t, n, r) {
  t.child = e === null ? lg(t, null, n, r) : ii(t, e.child, n, r);
}
function Bf(e, t, n, r, i) {
  n = n.render;
  var s = t.ref;
  return (
    $r(t, i),
    (r = Mc(e, t, n, r, s, i)),
    (n = Dc()),
    e !== null && !Qe
      ? ((t.updateQueue = e.updateQueue),
        (t.flags &= -2053),
        (e.lanes &= ~i),
        sn(e, t, i))
      : (ie && n && yc(t), (t.flags |= 1), Be(e, t, r, i), t.child)
  );
}
function Uf(e, t, n, r, i) {
  if (e === null) {
    var s = n.type;
    return typeof s == "function" &&
      !zc(s) &&
      s.defaultProps === void 0 &&
      n.compare === null &&
      n.defaultProps === void 0
      ? ((t.tag = 15), (t.type = s), Og(e, t, s, r, i))
      : ((e = vo(n.type, null, r, t, t.mode, i)),
        (e.ref = t.ref),
        (e.return = t),
        (t.child = e));
  }
  if (((s = e.child), !(e.lanes & i))) {
    var o = s.memoizedProps;
    if (
      ((n = n.compare), (n = n !== null ? n : rs), n(o, r) && e.ref === t.ref)
    )
      return sn(e, t, i);
  }
  return (
    (t.flags |= 1),
    (e = In(s, r)),
    (e.ref = t.ref),
    (e.return = t),
    (t.child = e)
  );
}
function Og(e, t, n, r, i) {
  if (e !== null) {
    var s = e.memoizedProps;
    if (rs(s, r) && e.ref === t.ref)
      if (((Qe = !1), (t.pendingProps = r = s), (e.lanes & i) !== 0))
        e.flags & 131072 && (Qe = !0);
      else return (t.lanes = e.lanes), sn(e, t, i);
  }
  return fu(e, t, n, r, i);
}
function jg(e, t, n) {
  var r = t.pendingProps,
    i = r.children,
    s = e !== null ? e.memoizedState : null;
  if (r.mode === "hidden")
    if (!(t.mode & 1))
      (t.memoizedState = { baseLanes: 0, cachePool: null, transitions: null }),
        ee(Lr, Je),
        (Je |= n);
    else {
      if (!(n & 1073741824))
        return (
          (e = s !== null ? s.baseLanes | n : n),
          (t.lanes = t.childLanes = 1073741824),
          (t.memoizedState = {
            baseLanes: e,
            cachePool: null,
            transitions: null,
          }),
          (t.updateQueue = null),
          ee(Lr, Je),
          (Je |= e),
          null
        );
      (t.memoizedState = { baseLanes: 0, cachePool: null, transitions: null }),
        (r = s !== null ? s.baseLanes : n),
        ee(Lr, Je),
        (Je |= r);
    }
  else
    s !== null ? ((r = s.baseLanes | n), (t.memoizedState = null)) : (r = n),
      ee(Lr, Je),
      (Je |= r);
  return Be(e, t, i, n), t.child;
}
function Ig(e, t) {
  var n = t.ref;
  ((e === null && n !== null) || (e !== null && e.ref !== n)) &&
    ((t.flags |= 512), (t.flags |= 2097152));
}
function fu(e, t, n, r, i) {
  var s = qe(n) ? dr : Fe.current;
  return (
    (s = ni(t, s)),
    $r(t, i),
    (n = Mc(e, t, n, r, s, i)),
    (r = Dc()),
    e !== null && !Qe
      ? ((t.updateQueue = e.updateQueue),
        (t.flags &= -2053),
        (e.lanes &= ~i),
        sn(e, t, i))
      : (ie && r && yc(t), (t.flags |= 1), Be(e, t, n, i), t.child)
  );
}
function $f(e, t, n, r, i) {
  if (qe(n)) {
    var s = !0;
    Oo(t);
  } else s = !1;
  if (($r(t, i), t.stateNode === null))
    mo(e, t), Ng(t, n, r), cu(t, n, r, i), (r = !0);
  else if (e === null) {
    var o = t.stateNode,
      a = t.memoizedProps;
    o.props = a;
    var l = o.context,
      u = n.contextType;
    typeof u == "object" && u !== null
      ? (u = gt(u))
      : ((u = qe(n) ? dr : Fe.current), (u = ni(t, u)));
    var c = n.getDerivedStateFromProps,
      d =
        typeof c == "function" ||
        typeof o.getSnapshotBeforeUpdate == "function";
    d ||
      (typeof o.UNSAFE_componentWillReceiveProps != "function" &&
        typeof o.componentWillReceiveProps != "function") ||
      ((a !== r || l !== u) && Ff(t, o, r, u)),
      (xn = !1);
    var f = t.memoizedState;
    (o.state = f),
      Vo(t, r, o, i),
      (l = t.memoizedState),
      a !== r || f !== l || Ge.current || xn
        ? (typeof c == "function" && (uu(t, n, c, r), (l = t.memoizedState)),
          (a = xn || If(t, n, a, r, f, l, u))
            ? (d ||
                (typeof o.UNSAFE_componentWillMount != "function" &&
                  typeof o.componentWillMount != "function") ||
                (typeof o.componentWillMount == "function" &&
                  o.componentWillMount(),
                typeof o.UNSAFE_componentWillMount == "function" &&
                  o.UNSAFE_componentWillMount()),
              typeof o.componentDidMount == "function" && (t.flags |= 4194308))
            : (typeof o.componentDidMount == "function" && (t.flags |= 4194308),
              (t.memoizedProps = r),
              (t.memoizedState = l)),
          (o.props = r),
          (o.state = l),
          (o.context = u),
          (r = a))
        : (typeof o.componentDidMount == "function" && (t.flags |= 4194308),
          (r = !1));
  } else {
    (o = t.stateNode),
      cg(e, t),
      (a = t.memoizedProps),
      (u = t.type === t.elementType ? a : St(t.type, a)),
      (o.props = u),
      (d = t.pendingProps),
      (f = o.context),
      (l = n.contextType),
      typeof l == "object" && l !== null
        ? (l = gt(l))
        : ((l = qe(n) ? dr : Fe.current), (l = ni(t, l)));
    var v = n.getDerivedStateFromProps;
    (c =
      typeof v == "function" ||
      typeof o.getSnapshotBeforeUpdate == "function") ||
      (typeof o.UNSAFE_componentWillReceiveProps != "function" &&
        typeof o.componentWillReceiveProps != "function") ||
      ((a !== d || f !== l) && Ff(t, o, r, l)),
      (xn = !1),
      (f = t.memoizedState),
      (o.state = f),
      Vo(t, r, o, i);
    var y = t.memoizedState;
    a !== d || f !== y || Ge.current || xn
      ? (typeof v == "function" && (uu(t, n, v, r), (y = t.memoizedState)),
        (u = xn || If(t, n, u, r, f, y, l) || !1)
          ? (c ||
              (typeof o.UNSAFE_componentWillUpdate != "function" &&
                typeof o.componentWillUpdate != "function") ||
              (typeof o.componentWillUpdate == "function" &&
                o.componentWillUpdate(r, y, l),
              typeof o.UNSAFE_componentWillUpdate == "function" &&
                o.UNSAFE_componentWillUpdate(r, y, l)),
            typeof o.componentDidUpdate == "function" && (t.flags |= 4),
            typeof o.getSnapshotBeforeUpdate == "function" && (t.flags |= 1024))
          : (typeof o.componentDidUpdate != "function" ||
              (a === e.memoizedProps && f === e.memoizedState) ||
              (t.flags |= 4),
            typeof o.getSnapshotBeforeUpdate != "function" ||
              (a === e.memoizedProps && f === e.memoizedState) ||
              (t.flags |= 1024),
            (t.memoizedProps = r),
            (t.memoizedState = y)),
        (o.props = r),
        (o.state = y),
        (o.context = l),
        (r = u))
      : (typeof o.componentDidUpdate != "function" ||
          (a === e.memoizedProps && f === e.memoizedState) ||
          (t.flags |= 4),
        typeof o.getSnapshotBeforeUpdate != "function" ||
          (a === e.memoizedProps && f === e.memoizedState) ||
          (t.flags |= 1024),
        (r = !1));
  }
  return hu(e, t, n, r, s, i);
}
function hu(e, t, n, r, i, s) {
  Ig(e, t);
  var o = (t.flags & 128) !== 0;
  if (!r && !o) return i && Rf(t, n, !1), sn(e, t, s);
  (r = t.stateNode), (rw.current = t);
  var a =
    o && typeof n.getDerivedStateFromError != "function" ? null : r.render();
  return (
    (t.flags |= 1),
    e !== null && o
      ? ((t.child = ii(t, e.child, null, s)), (t.child = ii(t, null, a, s)))
      : Be(e, t, a, s),
    (t.memoizedState = r.state),
    i && Rf(t, n, !0),
    t.child
  );
}
function Fg(e) {
  var t = e.stateNode;
  t.pendingContext
    ? Af(e, t.pendingContext, t.pendingContext !== t.context)
    : t.context && Af(e, t.context, !1),
    Tc(e, t.containerInfo);
}
function Wf(e, t, n, r, i) {
  return ri(), xc(i), (t.flags |= 256), Be(e, t, n, r), t.child;
}
var pu = { dehydrated: null, treeContext: null, retryLane: 0 };
function mu(e) {
  return { baseLanes: e, cachePool: null, transitions: null };
}
function _g(e, t, n) {
  var r = t.pendingProps,
    i = oe.current,
    s = !1,
    o = (t.flags & 128) !== 0,
    a;
  if (
    ((a = o) ||
      (a = e !== null && e.memoizedState === null ? !1 : (i & 2) !== 0),
    a
      ? ((s = !0), (t.flags &= -129))
      : (e === null || e.memoizedState !== null) && (i |= 1),
    ee(oe, i & 1),
    e === null)
  )
    return (
      au(t),
      (e = t.memoizedState),
      e !== null && ((e = e.dehydrated), e !== null)
        ? (t.mode & 1
            ? e.data === "$!"
              ? (t.lanes = 8)
              : (t.lanes = 1073741824)
            : (t.lanes = 1),
          null)
        : ((o = r.children),
          (e = r.fallback),
          s
            ? ((r = t.mode),
              (s = t.child),
              (o = { mode: "hidden", children: o }),
              !(r & 1) && s !== null
                ? ((s.childLanes = 0), (s.pendingProps = o))
                : (s = ga(o, r, 0, null)),
              (e = ur(e, r, n, null)),
              (s.return = t),
              (e.return = t),
              (s.sibling = e),
              (t.child = s),
              (t.child.memoizedState = mu(n)),
              (t.memoizedState = pu),
              e)
            : Lc(t, o))
    );
  if (((i = e.memoizedState), i !== null && ((a = i.dehydrated), a !== null)))
    return iw(e, t, o, r, a, i, n);
  if (s) {
    (s = r.fallback), (o = t.mode), (i = e.child), (a = i.sibling);
    var l = { mode: "hidden", children: r.children };
    return (
      !(o & 1) && t.child !== i
        ? ((r = t.child),
          (r.childLanes = 0),
          (r.pendingProps = l),
          (t.deletions = null))
        : ((r = In(i, l)), (r.subtreeFlags = i.subtreeFlags & 14680064)),
      a !== null ? (s = In(a, s)) : ((s = ur(s, o, n, null)), (s.flags |= 2)),
      (s.return = t),
      (r.return = t),
      (r.sibling = s),
      (t.child = r),
      (r = s),
      (s = t.child),
      (o = e.child.memoizedState),
      (o =
        o === null
          ? mu(n)
          : {
              baseLanes: o.baseLanes | n,
              cachePool: null,
              transitions: o.transitions,
            }),
      (s.memoizedState = o),
      (s.childLanes = e.childLanes & ~n),
      (t.memoizedState = pu),
      r
    );
  }
  return (
    (s = e.child),
    (e = s.sibling),
    (r = In(s, { mode: "visible", children: r.children })),
    !(t.mode & 1) && (r.lanes = n),
    (r.return = t),
    (r.sibling = null),
    e !== null &&
      ((n = t.deletions),
      n === null ? ((t.deletions = [e]), (t.flags |= 16)) : n.push(e)),
    (t.child = r),
    (t.memoizedState = null),
    r
  );
}
function Lc(e, t) {
  return (
    (t = ga({ mode: "visible", children: t }, e.mode, 0, null)),
    (t.return = e),
    (e.child = t)
  );
}
function Xs(e, t, n, r) {
  return (
    r !== null && xc(r),
    ii(t, e.child, null, n),
    (e = Lc(t, t.pendingProps.children)),
    (e.flags |= 2),
    (t.memoizedState = null),
    e
  );
}
function iw(e, t, n, r, i, s, o) {
  if (n)
    return t.flags & 256
      ? ((t.flags &= -257), (r = cl(Error(M(422)))), Xs(e, t, o, r))
      : t.memoizedState !== null
      ? ((t.child = e.child), (t.flags |= 128), null)
      : ((s = r.fallback),
        (i = t.mode),
        (r = ga({ mode: "visible", children: r.children }, i, 0, null)),
        (s = ur(s, i, o, null)),
        (s.flags |= 2),
        (r.return = t),
        (s.return = t),
        (r.sibling = s),
        (t.child = r),
        t.mode & 1 && ii(t, e.child, null, o),
        (t.child.memoizedState = mu(o)),
        (t.memoizedState = pu),
        s);
  if (!(t.mode & 1)) return Xs(e, t, o, null);
  if (i.data === "$!") {
    if (((r = i.nextSibling && i.nextSibling.dataset), r)) var a = r.dgst;
    return (r = a), (s = Error(M(419))), (r = cl(s, r, void 0)), Xs(e, t, o, r);
  }
  if (((a = (o & e.childLanes) !== 0), Qe || a)) {
    if (((r = Ee), r !== null)) {
      switch (o & -o) {
        case 4:
          i = 2;
          break;
        case 16:
          i = 8;
          break;
        case 64:
        case 128:
        case 256:
        case 512:
        case 1024:
        case 2048:
        case 4096:
        case 8192:
        case 16384:
        case 32768:
        case 65536:
        case 131072:
        case 262144:
        case 524288:
        case 1048576:
        case 2097152:
        case 4194304:
        case 8388608:
        case 16777216:
        case 33554432:
        case 67108864:
          i = 32;
          break;
        case 536870912:
          i = 268435456;
          break;
        default:
          i = 0;
      }
      (i = i & (r.suspendedLanes | o) ? 0 : i),
        i !== 0 &&
          i !== s.retryLane &&
          ((s.retryLane = i), rn(e, i), At(r, e, i, -1));
    }
    return Vc(), (r = cl(Error(M(421)))), Xs(e, t, o, r);
  }
  return i.data === "$?"
    ? ((t.flags |= 128),
      (t.child = e.child),
      (t = yw.bind(null, e)),
      (i._reactRetry = t),
      null)
    : ((e = s.treeContext),
      (tt = bn(i.nextSibling)),
      (nt = t),
      (ie = !0),
      (Tt = null),
      e !== null &&
        ((ft[ht++] = qt),
        (ft[ht++] = Xt),
        (ft[ht++] = fr),
        (qt = e.id),
        (Xt = e.overflow),
        (fr = t)),
      (t = Lc(t, r.children)),
      (t.flags |= 4096),
      t);
}
function Hf(e, t, n) {
  e.lanes |= t;
  var r = e.alternate;
  r !== null && (r.lanes |= t), lu(e.return, t, n);
}
function dl(e, t, n, r, i) {
  var s = e.memoizedState;
  s === null
    ? (e.memoizedState = {
        isBackwards: t,
        rendering: null,
        renderingStartTime: 0,
        last: r,
        tail: n,
        tailMode: i,
      })
    : ((s.isBackwards = t),
      (s.rendering = null),
      (s.renderingStartTime = 0),
      (s.last = r),
      (s.tail = n),
      (s.tailMode = i));
}
function Vg(e, t, n) {
  var r = t.pendingProps,
    i = r.revealOrder,
    s = r.tail;
  if ((Be(e, t, r.children, n), (r = oe.current), r & 2))
    (r = (r & 1) | 2), (t.flags |= 128);
  else {
    if (e !== null && e.flags & 128)
      e: for (e = t.child; e !== null; ) {
        if (e.tag === 13) e.memoizedState !== null && Hf(e, n, t);
        else if (e.tag === 19) Hf(e, n, t);
        else if (e.child !== null) {
          (e.child.return = e), (e = e.child);
          continue;
        }
        if (e === t) break e;
        for (; e.sibling === null; ) {
          if (e.return === null || e.return === t) break e;
          e = e.return;
        }
        (e.sibling.return = e.return), (e = e.sibling);
      }
    r &= 1;
  }
  if ((ee(oe, r), !(t.mode & 1))) t.memoizedState = null;
  else
    switch (i) {
      case "forwards":
        for (n = t.child, i = null; n !== null; )
          (e = n.alternate),
            e !== null && zo(e) === null && (i = n),
            (n = n.sibling);
        (n = i),
          n === null
            ? ((i = t.child), (t.child = null))
            : ((i = n.sibling), (n.sibling = null)),
          dl(t, !1, i, n, s);
        break;
      case "backwards":
        for (n = null, i = t.child, t.child = null; i !== null; ) {
          if (((e = i.alternate), e !== null && zo(e) === null)) {
            t.child = i;
            break;
          }
          (e = i.sibling), (i.sibling = n), (n = i), (i = e);
        }
        dl(t, !0, n, null, s);
        break;
      case "together":
        dl(t, !1, null, null, void 0);
        break;
      default:
        t.memoizedState = null;
    }
  return t.child;
}
function mo(e, t) {
  !(t.mode & 1) &&
    e !== null &&
    ((e.alternate = null), (t.alternate = null), (t.flags |= 2));
}
function sn(e, t, n) {
  if (
    (e !== null && (t.dependencies = e.dependencies),
    (pr |= t.lanes),
    !(n & t.childLanes))
  )
    return null;
  if (e !== null && t.child !== e.child) throw Error(M(153));
  if (t.child !== null) {
    for (
      e = t.child, n = In(e, e.pendingProps), t.child = n, n.return = t;
      e.sibling !== null;

    )
      (e = e.sibling), (n = n.sibling = In(e, e.pendingProps)), (n.return = t);
    n.sibling = null;
  }
  return t.child;
}
function sw(e, t, n) {
  switch (t.tag) {
    case 3:
      Fg(t), ri();
      break;
    case 5:
      dg(t);
      break;
    case 1:
      qe(t.type) && Oo(t);
      break;
    case 4:
      Tc(t, t.stateNode.containerInfo);
      break;
    case 10:
      var r = t.type._context,
        i = t.memoizedProps.value;
      ee(Fo, r._currentValue), (r._currentValue = i);
      break;
    case 13:
      if (((r = t.memoizedState), r !== null))
        return r.dehydrated !== null
          ? (ee(oe, oe.current & 1), (t.flags |= 128), null)
          : n & t.child.childLanes
          ? _g(e, t, n)
          : (ee(oe, oe.current & 1),
            (e = sn(e, t, n)),
            e !== null ? e.sibling : null);
      ee(oe, oe.current & 1);
      break;
    case 19:
      if (((r = (n & t.childLanes) !== 0), e.flags & 128)) {
        if (r) return Vg(e, t, n);
        t.flags |= 128;
      }
      if (
        ((i = t.memoizedState),
        i !== null &&
          ((i.rendering = null), (i.tail = null), (i.lastEffect = null)),
        ee(oe, oe.current),
        r)
      )
        break;
      return null;
    case 22:
    case 23:
      return (t.lanes = 0), jg(e, t, n);
  }
  return sn(e, t, n);
}
var zg, gu, Bg, Ug;
zg = function (e, t) {
  for (var n = t.child; n !== null; ) {
    if (n.tag === 5 || n.tag === 6) e.appendChild(n.stateNode);
    else if (n.tag !== 4 && n.child !== null) {
      (n.child.return = n), (n = n.child);
      continue;
    }
    if (n === t) break;
    for (; n.sibling === null; ) {
      if (n.return === null || n.return === t) return;
      n = n.return;
    }
    (n.sibling.return = n.return), (n = n.sibling);
  }
};
gu = function () {};
Bg = function (e, t, n, r) {
  var i = e.memoizedProps;
  if (i !== r) {
    (e = t.stateNode), tr(_t.current);
    var s = null;
    switch (n) {
      case "input":
        (i = _l(e, i)), (r = _l(e, r)), (s = []);
        break;
      case "select":
        (i = ce({}, i, { value: void 0 })),
          (r = ce({}, r, { value: void 0 })),
          (s = []);
        break;
      case "textarea":
        (i = Bl(e, i)), (r = Bl(e, r)), (s = []);
        break;
      default:
        typeof i.onClick != "function" &&
          typeof r.onClick == "function" &&
          (e.onclick = bo);
    }
    $l(n, r);
    var o;
    n = null;
    for (u in i)
      if (!r.hasOwnProperty(u) && i.hasOwnProperty(u) && i[u] != null)
        if (u === "style") {
          var a = i[u];
          for (o in a) a.hasOwnProperty(o) && (n || (n = {}), (n[o] = ""));
        } else
          u !== "dangerouslySetInnerHTML" &&
            u !== "children" &&
            u !== "suppressContentEditableWarning" &&
            u !== "suppressHydrationWarning" &&
            u !== "autoFocus" &&
            (Xi.hasOwnProperty(u)
              ? s || (s = [])
              : (s = s || []).push(u, null));
    for (u in r) {
      var l = r[u];
      if (
        ((a = i != null ? i[u] : void 0),
        r.hasOwnProperty(u) && l !== a && (l != null || a != null))
      )
        if (u === "style")
          if (a) {
            for (o in a)
              !a.hasOwnProperty(o) ||
                (l && l.hasOwnProperty(o)) ||
                (n || (n = {}), (n[o] = ""));
            for (o in l)
              l.hasOwnProperty(o) &&
                a[o] !== l[o] &&
                (n || (n = {}), (n[o] = l[o]));
          } else n || (s || (s = []), s.push(u, n)), (n = l);
        else
          u === "dangerouslySetInnerHTML"
            ? ((l = l ? l.__html : void 0),
              (a = a ? a.__html : void 0),
              l != null && a !== l && (s = s || []).push(u, l))
            : u === "children"
            ? (typeof l != "string" && typeof l != "number") ||
              (s = s || []).push(u, "" + l)
            : u !== "suppressContentEditableWarning" &&
              u !== "suppressHydrationWarning" &&
              (Xi.hasOwnProperty(u)
                ? (l != null && u === "onScroll" && ne("scroll", e),
                  s || a === l || (s = []))
                : (s = s || []).push(u, l));
    }
    n && (s = s || []).push("style", n);
    var u = s;
    (t.updateQueue = u) && (t.flags |= 4);
  }
};
Ug = function (e, t, n, r) {
  n !== r && (t.flags |= 4);
};
function Ei(e, t) {
  if (!ie)
    switch (e.tailMode) {
      case "hidden":
        t = e.tail;
        for (var n = null; t !== null; )
          t.alternate !== null && (n = t), (t = t.sibling);
        n === null ? (e.tail = null) : (n.sibling = null);
        break;
      case "collapsed":
        n = e.tail;
        for (var r = null; n !== null; )
          n.alternate !== null && (r = n), (n = n.sibling);
        r === null
          ? t || e.tail === null
            ? (e.tail = null)
            : (e.tail.sibling = null)
          : (r.sibling = null);
    }
}
function Ne(e) {
  var t = e.alternate !== null && e.alternate.child === e.child,
    n = 0,
    r = 0;
  if (t)
    for (var i = e.child; i !== null; )
      (n |= i.lanes | i.childLanes),
        (r |= i.subtreeFlags & 14680064),
        (r |= i.flags & 14680064),
        (i.return = e),
        (i = i.sibling);
  else
    for (i = e.child; i !== null; )
      (n |= i.lanes | i.childLanes),
        (r |= i.subtreeFlags),
        (r |= i.flags),
        (i.return = e),
        (i = i.sibling);
  return (e.subtreeFlags |= r), (e.childLanes = n), t;
}
function ow(e, t, n) {
  var r = t.pendingProps;
  switch ((vc(t), t.tag)) {
    case 2:
    case 16:
    case 15:
    case 0:
    case 11:
    case 7:
    case 8:
    case 12:
    case 9:
    case 14:
      return Ne(t), null;
    case 1:
      return qe(t.type) && Lo(), Ne(t), null;
    case 3:
      return (
        (r = t.stateNode),
        si(),
        re(Ge),
        re(Fe),
        Ac(),
        r.pendingContext &&
          ((r.context = r.pendingContext), (r.pendingContext = null)),
        (e === null || e.child === null) &&
          (Gs(t)
            ? (t.flags |= 4)
            : e === null ||
              (e.memoizedState.isDehydrated && !(t.flags & 256)) ||
              ((t.flags |= 1024), Tt !== null && (Eu(Tt), (Tt = null)))),
        gu(e, t),
        Ne(t),
        null
      );
    case 5:
      kc(t);
      var i = tr(ls.current);
      if (((n = t.type), e !== null && t.stateNode != null))
        Bg(e, t, n, r, i),
          e.ref !== t.ref && ((t.flags |= 512), (t.flags |= 2097152));
      else {
        if (!r) {
          if (t.stateNode === null) throw Error(M(166));
          return Ne(t), null;
        }
        if (((e = tr(_t.current)), Gs(t))) {
          (r = t.stateNode), (n = t.type);
          var s = t.memoizedProps;
          switch (((r[It] = t), (r[os] = s), (e = (t.mode & 1) !== 0), n)) {
            case "dialog":
              ne("cancel", r), ne("close", r);
              break;
            case "iframe":
            case "object":
            case "embed":
              ne("load", r);
              break;
            case "video":
            case "audio":
              for (i = 0; i < bi.length; i++) ne(bi[i], r);
              break;
            case "source":
              ne("error", r);
              break;
            case "img":
            case "image":
            case "link":
              ne("error", r), ne("load", r);
              break;
            case "details":
              ne("toggle", r);
              break;
            case "input":
              Jd(r, s), ne("invalid", r);
              break;
            case "select":
              (r._wrapperState = { wasMultiple: !!s.multiple }),
                ne("invalid", r);
              break;
            case "textarea":
              tf(r, s), ne("invalid", r);
          }
          $l(n, s), (i = null);
          for (var o in s)
            if (s.hasOwnProperty(o)) {
              var a = s[o];
              o === "children"
                ? typeof a == "string"
                  ? r.textContent !== a &&
                    (s.suppressHydrationWarning !== !0 &&
                      Qs(r.textContent, a, e),
                    (i = ["children", a]))
                  : typeof a == "number" &&
                    r.textContent !== "" + a &&
                    (s.suppressHydrationWarning !== !0 &&
                      Qs(r.textContent, a, e),
                    (i = ["children", "" + a]))
                : Xi.hasOwnProperty(o) &&
                  a != null &&
                  o === "onScroll" &&
                  ne("scroll", r);
            }
          switch (n) {
            case "input":
              Vs(r), ef(r, s, !0);
              break;
            case "textarea":
              Vs(r), nf(r);
              break;
            case "select":
            case "option":
              break;
            default:
              typeof s.onClick == "function" && (r.onclick = bo);
          }
          (r = i), (t.updateQueue = r), r !== null && (t.flags |= 4);
        } else {
          (o = i.nodeType === 9 ? i : i.ownerDocument),
            e === "http://www.w3.org/1999/xhtml" && (e = gm(n)),
            e === "http://www.w3.org/1999/xhtml"
              ? n === "script"
                ? ((e = o.createElement("div")),
                  (e.innerHTML = "<script></script>"),
                  (e = e.removeChild(e.firstChild)))
                : typeof r.is == "string"
                ? (e = o.createElement(n, { is: r.is }))
                : ((e = o.createElement(n)),
                  n === "select" &&
                    ((o = e),
                    r.multiple
                      ? (o.multiple = !0)
                      : r.size && (o.size = r.size)))
              : (e = o.createElementNS(e, n)),
            (e[It] = t),
            (e[os] = r),
            zg(e, t, !1, !1),
            (t.stateNode = e);
          e: {
            switch (((o = Wl(n, r)), n)) {
              case "dialog":
                ne("cancel", e), ne("close", e), (i = r);
                break;
              case "iframe":
              case "object":
              case "embed":
                ne("load", e), (i = r);
                break;
              case "video":
              case "audio":
                for (i = 0; i < bi.length; i++) ne(bi[i], e);
                i = r;
                break;
              case "source":
                ne("error", e), (i = r);
                break;
              case "img":
              case "image":
              case "link":
                ne("error", e), ne("load", e), (i = r);
                break;
              case "details":
                ne("toggle", e), (i = r);
                break;
              case "input":
                Jd(e, r), (i = _l(e, r)), ne("invalid", e);
                break;
              case "option":
                i = r;
                break;
              case "select":
                (e._wrapperState = { wasMultiple: !!r.multiple }),
                  (i = ce({}, r, { value: void 0 })),
                  ne("invalid", e);
                break;
              case "textarea":
                tf(e, r), (i = Bl(e, r)), ne("invalid", e);
                break;
              default:
                i = r;
            }
            $l(n, i), (a = i);
            for (s in a)
              if (a.hasOwnProperty(s)) {
                var l = a[s];
                s === "style"
                  ? xm(e, l)
                  : s === "dangerouslySetInnerHTML"
                  ? ((l = l ? l.__html : void 0), l != null && ym(e, l))
                  : s === "children"
                  ? typeof l == "string"
                    ? (n !== "textarea" || l !== "") && Yi(e, l)
                    : typeof l == "number" && Yi(e, "" + l)
                  : s !== "suppressContentEditableWarning" &&
                    s !== "suppressHydrationWarning" &&
                    s !== "autoFocus" &&
                    (Xi.hasOwnProperty(s)
                      ? l != null && s === "onScroll" && ne("scroll", e)
                      : l != null && rc(e, s, l, o));
              }
            switch (n) {
              case "input":
                Vs(e), ef(e, r, !1);
                break;
              case "textarea":
                Vs(e), nf(e);
                break;
              case "option":
                r.value != null && e.setAttribute("value", "" + Vn(r.value));
                break;
              case "select":
                (e.multiple = !!r.multiple),
                  (s = r.value),
                  s != null
                    ? Vr(e, !!r.multiple, s, !1)
                    : r.defaultValue != null &&
                      Vr(e, !!r.multiple, r.defaultValue, !0);
                break;
              default:
                typeof i.onClick == "function" && (e.onclick = bo);
            }
            switch (n) {
              case "button":
              case "input":
              case "select":
              case "textarea":
                r = !!r.autoFocus;
                break e;
              case "img":
                r = !0;
                break e;
              default:
                r = !1;
            }
          }
          r && (t.flags |= 4);
        }
        t.ref !== null && ((t.flags |= 512), (t.flags |= 2097152));
      }
      return Ne(t), null;
    case 6:
      if (e && t.stateNode != null) Ug(e, t, e.memoizedProps, r);
      else {
        if (typeof r != "string" && t.stateNode === null) throw Error(M(166));
        if (((n = tr(ls.current)), tr(_t.current), Gs(t))) {
          if (
            ((r = t.stateNode),
            (n = t.memoizedProps),
            (r[It] = t),
            (s = r.nodeValue !== n) && ((e = nt), e !== null))
          )
            switch (e.tag) {
              case 3:
                Qs(r.nodeValue, n, (e.mode & 1) !== 0);
                break;
              case 5:
                e.memoizedProps.suppressHydrationWarning !== !0 &&
                  Qs(r.nodeValue, n, (e.mode & 1) !== 0);
            }
          s && (t.flags |= 4);
        } else
          (r = (n.nodeType === 9 ? n : n.ownerDocument).createTextNode(r)),
            (r[It] = t),
            (t.stateNode = r);
      }
      return Ne(t), null;
    case 13:
      if (
        (re(oe),
        (r = t.memoizedState),
        e === null ||
          (e.memoizedState !== null && e.memoizedState.dehydrated !== null))
      ) {
        if (ie && tt !== null && t.mode & 1 && !(t.flags & 128))
          og(), ri(), (t.flags |= 98560), (s = !1);
        else if (((s = Gs(t)), r !== null && r.dehydrated !== null)) {
          if (e === null) {
            if (!s) throw Error(M(318));
            if (
              ((s = t.memoizedState),
              (s = s !== null ? s.dehydrated : null),
              !s)
            )
              throw Error(M(317));
            s[It] = t;
          } else
            ri(), !(t.flags & 128) && (t.memoizedState = null), (t.flags |= 4);
          Ne(t), (s = !1);
        } else Tt !== null && (Eu(Tt), (Tt = null)), (s = !0);
        if (!s) return t.flags & 65536 ? t : null;
      }
      return t.flags & 128
        ? ((t.lanes = n), t)
        : ((r = r !== null),
          r !== (e !== null && e.memoizedState !== null) &&
            r &&
            ((t.child.flags |= 8192),
            t.mode & 1 &&
              (e === null || oe.current & 1 ? Se === 0 && (Se = 3) : Vc())),
          t.updateQueue !== null && (t.flags |= 4),
          Ne(t),
          null);
    case 4:
      return (
        si(), gu(e, t), e === null && is(t.stateNode.containerInfo), Ne(t), null
      );
    case 10:
      return Pc(t.type._context), Ne(t), null;
    case 17:
      return qe(t.type) && Lo(), Ne(t), null;
    case 19:
      if ((re(oe), (s = t.memoizedState), s === null)) return Ne(t), null;
      if (((r = (t.flags & 128) !== 0), (o = s.rendering), o === null))
        if (r) Ei(s, !1);
        else {
          if (Se !== 0 || (e !== null && e.flags & 128))
            for (e = t.child; e !== null; ) {
              if (((o = zo(e)), o !== null)) {
                for (
                  t.flags |= 128,
                    Ei(s, !1),
                    r = o.updateQueue,
                    r !== null && ((t.updateQueue = r), (t.flags |= 4)),
                    t.subtreeFlags = 0,
                    r = n,
                    n = t.child;
                  n !== null;

                )
                  (s = n),
                    (e = r),
                    (s.flags &= 14680066),
                    (o = s.alternate),
                    o === null
                      ? ((s.childLanes = 0),
                        (s.lanes = e),
                        (s.child = null),
                        (s.subtreeFlags = 0),
                        (s.memoizedProps = null),
                        (s.memoizedState = null),
                        (s.updateQueue = null),
                        (s.dependencies = null),
                        (s.stateNode = null))
                      : ((s.childLanes = o.childLanes),
                        (s.lanes = o.lanes),
                        (s.child = o.child),
                        (s.subtreeFlags = 0),
                        (s.deletions = null),
                        (s.memoizedProps = o.memoizedProps),
                        (s.memoizedState = o.memoizedState),
                        (s.updateQueue = o.updateQueue),
                        (s.type = o.type),
                        (e = o.dependencies),
                        (s.dependencies =
                          e === null
                            ? null
                            : {
                                lanes: e.lanes,
                                firstContext: e.firstContext,
                              })),
                    (n = n.sibling);
                return ee(oe, (oe.current & 1) | 2), t.child;
              }
              e = e.sibling;
            }
          s.tail !== null &&
            me() > ai &&
            ((t.flags |= 128), (r = !0), Ei(s, !1), (t.lanes = 4194304));
        }
      else {
        if (!r)
          if (((e = zo(o)), e !== null)) {
            if (
              ((t.flags |= 128),
              (r = !0),
              (n = e.updateQueue),
              n !== null && ((t.updateQueue = n), (t.flags |= 4)),
              Ei(s, !0),
              s.tail === null && s.tailMode === "hidden" && !o.alternate && !ie)
            )
              return Ne(t), null;
          } else
            2 * me() - s.renderingStartTime > ai &&
              n !== 1073741824 &&
              ((t.flags |= 128), (r = !0), Ei(s, !1), (t.lanes = 4194304));
        s.isBackwards
          ? ((o.sibling = t.child), (t.child = o))
          : ((n = s.last),
            n !== null ? (n.sibling = o) : (t.child = o),
            (s.last = o));
      }
      return s.tail !== null
        ? ((t = s.tail),
          (s.rendering = t),
          (s.tail = t.sibling),
          (s.renderingStartTime = me()),
          (t.sibling = null),
          (n = oe.current),
          ee(oe, r ? (n & 1) | 2 : n & 1),
          t)
        : (Ne(t), null);
    case 22:
    case 23:
      return (
        _c(),
        (r = t.memoizedState !== null),
        e !== null && (e.memoizedState !== null) !== r && (t.flags |= 8192),
        r && t.mode & 1
          ? Je & 1073741824 && (Ne(t), t.subtreeFlags & 6 && (t.flags |= 8192))
          : Ne(t),
        null
      );
    case 24:
      return null;
    case 25:
      return null;
  }
  throw Error(M(156, t.tag));
}
function aw(e, t) {
  switch ((vc(t), t.tag)) {
    case 1:
      return (
        qe(t.type) && Lo(),
        (e = t.flags),
        e & 65536 ? ((t.flags = (e & -65537) | 128), t) : null
      );
    case 3:
      return (
        si(),
        re(Ge),
        re(Fe),
        Ac(),
        (e = t.flags),
        e & 65536 && !(e & 128) ? ((t.flags = (e & -65537) | 128), t) : null
      );
    case 5:
      return kc(t), null;
    case 13:
      if (
        (re(oe), (e = t.memoizedState), e !== null && e.dehydrated !== null)
      ) {
        if (t.alternate === null) throw Error(M(340));
        ri();
      }
      return (
        (e = t.flags), e & 65536 ? ((t.flags = (e & -65537) | 128), t) : null
      );
    case 19:
      return re(oe), null;
    case 4:
      return si(), null;
    case 10:
      return Pc(t.type._context), null;
    case 22:
    case 23:
      return _c(), null;
    case 24:
      return null;
    default:
      return null;
  }
}
var Ys = !1,
  Oe = !1,
  lw = typeof WeakSet == "function" ? WeakSet : Set,
  O = null;
function br(e, t) {
  var n = e.ref;
  if (n !== null)
    if (typeof n == "function")
      try {
        n(null);
      } catch (r) {
        he(e, t, r);
      }
    else n.current = null;
}
function yu(e, t, n) {
  try {
    n();
  } catch (r) {
    he(e, t, r);
  }
}
var Kf = !1;
function uw(e, t) {
  if (((eu = Mo), (e = Qm()), gc(e))) {
    if ("selectionStart" in e)
      var n = { start: e.selectionStart, end: e.selectionEnd };
    else
      e: {
        n = ((n = e.ownerDocument) && n.defaultView) || window;
        var r = n.getSelection && n.getSelection();
        if (r && r.rangeCount !== 0) {
          n = r.anchorNode;
          var i = r.anchorOffset,
            s = r.focusNode;
          r = r.focusOffset;
          try {
            n.nodeType, s.nodeType;
          } catch {
            n = null;
            break e;
          }
          var o = 0,
            a = -1,
            l = -1,
            u = 0,
            c = 0,
            d = e,
            f = null;
          t: for (;;) {
            for (
              var v;
              d !== n || (i !== 0 && d.nodeType !== 3) || (a = o + i),
                d !== s || (r !== 0 && d.nodeType !== 3) || (l = o + r),
                d.nodeType === 3 && (o += d.nodeValue.length),
                (v = d.firstChild) !== null;

            )
              (f = d), (d = v);
            for (;;) {
              if (d === e) break t;
              if (
                (f === n && ++u === i && (a = o),
                f === s && ++c === r && (l = o),
                (v = d.nextSibling) !== null)
              )
                break;
              (d = f), (f = d.parentNode);
            }
            d = v;
          }
          n = a === -1 || l === -1 ? null : { start: a, end: l };
        } else n = null;
      }
    n = n || { start: 0, end: 0 };
  } else n = null;
  for (tu = { focusedElem: e, selectionRange: n }, Mo = !1, O = t; O !== null; )
    if (((t = O), (e = t.child), (t.subtreeFlags & 1028) !== 0 && e !== null))
      (e.return = t), (O = e);
    else
      for (; O !== null; ) {
        t = O;
        try {
          var y = t.alternate;
          if (t.flags & 1024)
            switch (t.tag) {
              case 0:
              case 11:
              case 15:
                break;
              case 1:
                if (y !== null) {
                  var m = y.memoizedProps,
                    x = y.memoizedState,
                    h = t.stateNode,
                    p = h.getSnapshotBeforeUpdate(
                      t.elementType === t.type ? m : St(t.type, m),
                      x
                    );
                  h.__reactInternalSnapshotBeforeUpdate = p;
                }
                break;
              case 3:
                var g = t.stateNode.containerInfo;
                g.nodeType === 1
                  ? (g.textContent = "")
                  : g.nodeType === 9 &&
                    g.documentElement &&
                    g.removeChild(g.documentElement);
                break;
              case 5:
              case 6:
              case 4:
              case 17:
                break;
              default:
                throw Error(M(163));
            }
        } catch (S) {
          he(t, t.return, S);
        }
        if (((e = t.sibling), e !== null)) {
          (e.return = t.return), (O = e);
          break;
        }
        O = t.return;
      }
  return (y = Kf), (Kf = !1), y;
}
function Ui(e, t, n) {
  var r = t.updateQueue;
  if (((r = r !== null ? r.lastEffect : null), r !== null)) {
    var i = (r = r.next);
    do {
      if ((i.tag & e) === e) {
        var s = i.destroy;
        (i.destroy = void 0), s !== void 0 && yu(t, n, s);
      }
      i = i.next;
    } while (i !== r);
  }
}
function pa(e, t) {
  if (
    ((t = t.updateQueue), (t = t !== null ? t.lastEffect : null), t !== null)
  ) {
    var n = (t = t.next);
    do {
      if ((n.tag & e) === e) {
        var r = n.create;
        n.destroy = r();
      }
      n = n.next;
    } while (n !== t);
  }
}
function vu(e) {
  var t = e.ref;
  if (t !== null) {
    var n = e.stateNode;
    switch (e.tag) {
      case 5:
        e = n;
        break;
      default:
        e = n;
    }
    typeof t == "function" ? t(e) : (t.current = e);
  }
}
function $g(e) {
  var t = e.alternate;
  t !== null && ((e.alternate = null), $g(t)),
    (e.child = null),
    (e.deletions = null),
    (e.sibling = null),
    e.tag === 5 &&
      ((t = e.stateNode),
      t !== null &&
        (delete t[It], delete t[os], delete t[iu], delete t[Hx], delete t[Kx])),
    (e.stateNode = null),
    (e.return = null),
    (e.dependencies = null),
    (e.memoizedProps = null),
    (e.memoizedState = null),
    (e.pendingProps = null),
    (e.stateNode = null),
    (e.updateQueue = null);
}
function Wg(e) {
  return e.tag === 5 || e.tag === 3 || e.tag === 4;
}
function Qf(e) {
  e: for (;;) {
    for (; e.sibling === null; ) {
      if (e.return === null || Wg(e.return)) return null;
      e = e.return;
    }
    for (
      e.sibling.return = e.return, e = e.sibling;
      e.tag !== 5 && e.tag !== 6 && e.tag !== 18;

    ) {
      if (e.flags & 2 || e.child === null || e.tag === 4) continue e;
      (e.child.return = e), (e = e.child);
    }
    if (!(e.flags & 2)) return e.stateNode;
  }
}
function xu(e, t, n) {
  var r = e.tag;
  if (r === 5 || r === 6)
    (e = e.stateNode),
      t
        ? n.nodeType === 8
          ? n.parentNode.insertBefore(e, t)
          : n.insertBefore(e, t)
        : (n.nodeType === 8
            ? ((t = n.parentNode), t.insertBefore(e, n))
            : ((t = n), t.appendChild(e)),
          (n = n._reactRootContainer),
          n != null || t.onclick !== null || (t.onclick = bo));
  else if (r !== 4 && ((e = e.child), e !== null))
    for (xu(e, t, n), e = e.sibling; e !== null; ) xu(e, t, n), (e = e.sibling);
}
function wu(e, t, n) {
  var r = e.tag;
  if (r === 5 || r === 6)
    (e = e.stateNode), t ? n.insertBefore(e, t) : n.appendChild(e);
  else if (r !== 4 && ((e = e.child), e !== null))
    for (wu(e, t, n), e = e.sibling; e !== null; ) wu(e, t, n), (e = e.sibling);
}
var Te = null,
  Et = !1;
function fn(e, t, n) {
  for (n = n.child; n !== null; ) Hg(e, t, n), (n = n.sibling);
}
function Hg(e, t, n) {
  if (Ft && typeof Ft.onCommitFiberUnmount == "function")
    try {
      Ft.onCommitFiberUnmount(oa, n);
    } catch {}
  switch (n.tag) {
    case 5:
      Oe || br(n, t);
    case 6:
      var r = Te,
        i = Et;
      (Te = null),
        fn(e, t, n),
        (Te = r),
        (Et = i),
        Te !== null &&
          (Et
            ? ((e = Te),
              (n = n.stateNode),
              e.nodeType === 8 ? e.parentNode.removeChild(n) : e.removeChild(n))
            : Te.removeChild(n.stateNode));
      break;
    case 18:
      Te !== null &&
        (Et
          ? ((e = Te),
            (n = n.stateNode),
            e.nodeType === 8
              ? il(e.parentNode, n)
              : e.nodeType === 1 && il(e, n),
            ts(e))
          : il(Te, n.stateNode));
      break;
    case 4:
      (r = Te),
        (i = Et),
        (Te = n.stateNode.containerInfo),
        (Et = !0),
        fn(e, t, n),
        (Te = r),
        (Et = i);
      break;
    case 0:
    case 11:
    case 14:
    case 15:
      if (
        !Oe &&
        ((r = n.updateQueue), r !== null && ((r = r.lastEffect), r !== null))
      ) {
        i = r = r.next;
        do {
          var s = i,
            o = s.destroy;
          (s = s.tag),
            o !== void 0 && (s & 2 || s & 4) && yu(n, t, o),
            (i = i.next);
        } while (i !== r);
      }
      fn(e, t, n);
      break;
    case 1:
      if (
        !Oe &&
        (br(n, t),
        (r = n.stateNode),
        typeof r.componentWillUnmount == "function")
      )
        try {
          (r.props = n.memoizedProps),
            (r.state = n.memoizedState),
            r.componentWillUnmount();
        } catch (a) {
          he(n, t, a);
        }
      fn(e, t, n);
      break;
    case 21:
      fn(e, t, n);
      break;
    case 22:
      n.mode & 1
        ? ((Oe = (r = Oe) || n.memoizedState !== null), fn(e, t, n), (Oe = r))
        : fn(e, t, n);
      break;
    default:
      fn(e, t, n);
  }
}
function Gf(e) {
  var t = e.updateQueue;
  if (t !== null) {
    e.updateQueue = null;
    var n = e.stateNode;
    n === null && (n = e.stateNode = new lw()),
      t.forEach(function (r) {
        var i = vw.bind(null, e, r);
        n.has(r) || (n.add(r), r.then(i, i));
      });
  }
}
function xt(e, t) {
  var n = t.deletions;
  if (n !== null)
    for (var r = 0; r < n.length; r++) {
      var i = n[r];
      try {
        var s = e,
          o = t,
          a = o;
        e: for (; a !== null; ) {
          switch (a.tag) {
            case 5:
              (Te = a.stateNode), (Et = !1);
              break e;
            case 3:
              (Te = a.stateNode.containerInfo), (Et = !0);
              break e;
            case 4:
              (Te = a.stateNode.containerInfo), (Et = !0);
              break e;
          }
          a = a.return;
        }
        if (Te === null) throw Error(M(160));
        Hg(s, o, i), (Te = null), (Et = !1);
        var l = i.alternate;
        l !== null && (l.return = null), (i.return = null);
      } catch (u) {
        he(i, t, u);
      }
    }
  if (t.subtreeFlags & 12854)
    for (t = t.child; t !== null; ) Kg(t, e), (t = t.sibling);
}
function Kg(e, t) {
  var n = e.alternate,
    r = e.flags;
  switch (e.tag) {
    case 0:
    case 11:
    case 14:
    case 15:
      if ((xt(t, e), Nt(e), r & 4)) {
        try {
          Ui(3, e, e.return), pa(3, e);
        } catch (m) {
          he(e, e.return, m);
        }
        try {
          Ui(5, e, e.return);
        } catch (m) {
          he(e, e.return, m);
        }
      }
      break;
    case 1:
      xt(t, e), Nt(e), r & 512 && n !== null && br(n, n.return);
      break;
    case 5:
      if (
        (xt(t, e),
        Nt(e),
        r & 512 && n !== null && br(n, n.return),
        e.flags & 32)
      ) {
        var i = e.stateNode;
        try {
          Yi(i, "");
        } catch (m) {
          he(e, e.return, m);
        }
      }
      if (r & 4 && ((i = e.stateNode), i != null)) {
        var s = e.memoizedProps,
          o = n !== null ? n.memoizedProps : s,
          a = e.type,
          l = e.updateQueue;
        if (((e.updateQueue = null), l !== null))
          try {
            a === "input" && s.type === "radio" && s.name != null && pm(i, s),
              Wl(a, o);
            var u = Wl(a, s);
            for (o = 0; o < l.length; o += 2) {
              var c = l[o],
                d = l[o + 1];
              c === "style"
                ? xm(i, d)
                : c === "dangerouslySetInnerHTML"
                ? ym(i, d)
                : c === "children"
                ? Yi(i, d)
                : rc(i, c, d, u);
            }
            switch (a) {
              case "input":
                Vl(i, s);
                break;
              case "textarea":
                mm(i, s);
                break;
              case "select":
                var f = i._wrapperState.wasMultiple;
                i._wrapperState.wasMultiple = !!s.multiple;
                var v = s.value;
                v != null
                  ? Vr(i, !!s.multiple, v, !1)
                  : f !== !!s.multiple &&
                    (s.defaultValue != null
                      ? Vr(i, !!s.multiple, s.defaultValue, !0)
                      : Vr(i, !!s.multiple, s.multiple ? [] : "", !1));
            }
            i[os] = s;
          } catch (m) {
            he(e, e.return, m);
          }
      }
      break;
    case 6:
      if ((xt(t, e), Nt(e), r & 4)) {
        if (e.stateNode === null) throw Error(M(162));
        (i = e.stateNode), (s = e.memoizedProps);
        try {
          i.nodeValue = s;
        } catch (m) {
          he(e, e.return, m);
        }
      }
      break;
    case 3:
      if (
        (xt(t, e), Nt(e), r & 4 && n !== null && n.memoizedState.isDehydrated)
      )
        try {
          ts(t.containerInfo);
        } catch (m) {
          he(e, e.return, m);
        }
      break;
    case 4:
      xt(t, e), Nt(e);
      break;
    case 13:
      xt(t, e),
        Nt(e),
        (i = e.child),
        i.flags & 8192 &&
          ((s = i.memoizedState !== null),
          (i.stateNode.isHidden = s),
          !s ||
            (i.alternate !== null && i.alternate.memoizedState !== null) ||
            (Ic = me())),
        r & 4 && Gf(e);
      break;
    case 22:
      if (
        ((c = n !== null && n.memoizedState !== null),
        e.mode & 1 ? ((Oe = (u = Oe) || c), xt(t, e), (Oe = u)) : xt(t, e),
        Nt(e),
        r & 8192)
      ) {
        if (
          ((u = e.memoizedState !== null),
          (e.stateNode.isHidden = u) && !c && e.mode & 1)
        )
          for (O = e, c = e.child; c !== null; ) {
            for (d = O = c; O !== null; ) {
              switch (((f = O), (v = f.child), f.tag)) {
                case 0:
                case 11:
                case 14:
                case 15:
                  Ui(4, f, f.return);
                  break;
                case 1:
                  br(f, f.return);
                  var y = f.stateNode;
                  if (typeof y.componentWillUnmount == "function") {
                    (r = f), (n = f.return);
                    try {
                      (t = r),
                        (y.props = t.memoizedProps),
                        (y.state = t.memoizedState),
                        y.componentWillUnmount();
                    } catch (m) {
                      he(r, n, m);
                    }
                  }
                  break;
                case 5:
                  br(f, f.return);
                  break;
                case 22:
                  if (f.memoizedState !== null) {
                    Xf(d);
                    continue;
                  }
              }
              v !== null ? ((v.return = f), (O = v)) : Xf(d);
            }
            c = c.sibling;
          }
        e: for (c = null, d = e; ; ) {
          if (d.tag === 5) {
            if (c === null) {
              c = d;
              try {
                (i = d.stateNode),
                  u
                    ? ((s = i.style),
                      typeof s.setProperty == "function"
                        ? s.setProperty("display", "none", "important")
                        : (s.display = "none"))
                    : ((a = d.stateNode),
                      (l = d.memoizedProps.style),
                      (o =
                        l != null && l.hasOwnProperty("display")
                          ? l.display
                          : null),
                      (a.style.display = vm("display", o)));
              } catch (m) {
                he(e, e.return, m);
              }
            }
          } else if (d.tag === 6) {
            if (c === null)
              try {
                d.stateNode.nodeValue = u ? "" : d.memoizedProps;
              } catch (m) {
                he(e, e.return, m);
              }
          } else if (
            ((d.tag !== 22 && d.tag !== 23) ||
              d.memoizedState === null ||
              d === e) &&
            d.child !== null
          ) {
            (d.child.return = d), (d = d.child);
            continue;
          }
          if (d === e) break e;
          for (; d.sibling === null; ) {
            if (d.return === null || d.return === e) break e;
            c === d && (c = null), (d = d.return);
          }
          c === d && (c = null), (d.sibling.return = d.return), (d = d.sibling);
        }
      }
      break;
    case 19:
      xt(t, e), Nt(e), r & 4 && Gf(e);
      break;
    case 21:
      break;
    default:
      xt(t, e), Nt(e);
  }
}
function Nt(e) {
  var t = e.flags;
  if (t & 2) {
    try {
      e: {
        for (var n = e.return; n !== null; ) {
          if (Wg(n)) {
            var r = n;
            break e;
          }
          n = n.return;
        }
        throw Error(M(160));
      }
      switch (r.tag) {
        case 5:
          var i = r.stateNode;
          r.flags & 32 && (Yi(i, ""), (r.flags &= -33));
          var s = Qf(e);
          wu(e, s, i);
          break;
        case 3:
        case 4:
          var o = r.stateNode.containerInfo,
            a = Qf(e);
          xu(e, a, o);
          break;
        default:
          throw Error(M(161));
      }
    } catch (l) {
      he(e, e.return, l);
    }
    e.flags &= -3;
  }
  t & 4096 && (e.flags &= -4097);
}
function cw(e, t, n) {
  (O = e), Qg(e);
}
function Qg(e, t, n) {
  for (var r = (e.mode & 1) !== 0; O !== null; ) {
    var i = O,
      s = i.child;
    if (i.tag === 22 && r) {
      var o = i.memoizedState !== null || Ys;
      if (!o) {
        var a = i.alternate,
          l = (a !== null && a.memoizedState !== null) || Oe;
        a = Ys;
        var u = Oe;
        if (((Ys = o), (Oe = l) && !u))
          for (O = i; O !== null; )
            (o = O),
              (l = o.child),
              o.tag === 22 && o.memoizedState !== null
                ? Yf(i)
                : l !== null
                ? ((l.return = o), (O = l))
                : Yf(i);
        for (; s !== null; ) (O = s), Qg(s), (s = s.sibling);
        (O = i), (Ys = a), (Oe = u);
      }
      qf(e);
    } else
      i.subtreeFlags & 8772 && s !== null ? ((s.return = i), (O = s)) : qf(e);
  }
}
function qf(e) {
  for (; O !== null; ) {
    var t = O;
    if (t.flags & 8772) {
      var n = t.alternate;
      try {
        if (t.flags & 8772)
          switch (t.tag) {
            case 0:
            case 11:
            case 15:
              Oe || pa(5, t);
              break;
            case 1:
              var r = t.stateNode;
              if (t.flags & 4 && !Oe)
                if (n === null) r.componentDidMount();
                else {
                  var i =
                    t.elementType === t.type
                      ? n.memoizedProps
                      : St(t.type, n.memoizedProps);
                  r.componentDidUpdate(
                    i,
                    n.memoizedState,
                    r.__reactInternalSnapshotBeforeUpdate
                  );
                }
              var s = t.updateQueue;
              s !== null && Lf(t, s, r);
              break;
            case 3:
              var o = t.updateQueue;
              if (o !== null) {
                if (((n = null), t.child !== null))
                  switch (t.child.tag) {
                    case 5:
                      n = t.child.stateNode;
                      break;
                    case 1:
                      n = t.child.stateNode;
                  }
                Lf(t, o, n);
              }
              break;
            case 5:
              var a = t.stateNode;
              if (n === null && t.flags & 4) {
                n = a;
                var l = t.memoizedProps;
                switch (t.type) {
                  case "button":
                  case "input":
                  case "select":
                  case "textarea":
                    l.autoFocus && n.focus();
                    break;
                  case "img":
                    l.src && (n.src = l.src);
                }
              }
              break;
            case 6:
              break;
            case 4:
              break;
            case 12:
              break;
            case 13:
              if (t.memoizedState === null) {
                var u = t.alternate;
                if (u !== null) {
                  var c = u.memoizedState;
                  if (c !== null) {
                    var d = c.dehydrated;
                    d !== null && ts(d);
                  }
                }
              }
              break;
            case 19:
            case 17:
            case 21:
            case 22:
            case 23:
            case 25:
              break;
            default:
              throw Error(M(163));
          }
        Oe || (t.flags & 512 && vu(t));
      } catch (f) {
        he(t, t.return, f);
      }
    }
    if (t === e) {
      O = null;
      break;
    }
    if (((n = t.sibling), n !== null)) {
      (n.return = t.return), (O = n);
      break;
    }
    O = t.return;
  }
}
function Xf(e) {
  for (; O !== null; ) {
    var t = O;
    if (t === e) {
      O = null;
      break;
    }
    var n = t.sibling;
    if (n !== null) {
      (n.return = t.return), (O = n);
      break;
    }
    O = t.return;
  }
}
function Yf(e) {
  for (; O !== null; ) {
    var t = O;
    try {
      switch (t.tag) {
        case 0:
        case 11:
        case 15:
          var n = t.return;
          try {
            pa(4, t);
          } catch (l) {
            he(t, n, l);
          }
          break;
        case 1:
          var r = t.stateNode;
          if (typeof r.componentDidMount == "function") {
            var i = t.return;
            try {
              r.componentDidMount();
            } catch (l) {
              he(t, i, l);
            }
          }
          var s = t.return;
          try {
            vu(t);
          } catch (l) {
            he(t, s, l);
          }
          break;
        case 5:
          var o = t.return;
          try {
            vu(t);
          } catch (l) {
            he(t, o, l);
          }
      }
    } catch (l) {
      he(t, t.return, l);
    }
    if (t === e) {
      O = null;
      break;
    }
    var a = t.sibling;
    if (a !== null) {
      (a.return = t.return), (O = a);
      break;
    }
    O = t.return;
  }
}
var dw = Math.ceil,
  $o = ln.ReactCurrentDispatcher,
  Oc = ln.ReactCurrentOwner,
  mt = ln.ReactCurrentBatchConfig,
  K = 0,
  Ee = null,
  ve = null,
  Ae = 0,
  Je = 0,
  Lr = Wn(0),
  Se = 0,
  fs = null,
  pr = 0,
  ma = 0,
  jc = 0,
  $i = null,
  Ke = null,
  Ic = 0,
  ai = 1 / 0,
  Qt = null,
  Wo = !1,
  Su = null,
  On = null,
  Zs = !1,
  Rn = null,
  Ho = 0,
  Wi = 0,
  Pu = null,
  go = -1,
  yo = 0;
function $e() {
  return K & 6 ? me() : go !== -1 ? go : (go = me());
}
function jn(e) {
  return e.mode & 1
    ? K & 2 && Ae !== 0
      ? Ae & -Ae
      : Gx.transition !== null
      ? (yo === 0 && (yo = Nm()), yo)
      : ((e = X),
        e !== 0 || ((e = window.event), (e = e === void 0 ? 16 : _m(e.type))),
        e)
    : 1;
}
function At(e, t, n, r) {
  if (50 < Wi) throw ((Wi = 0), (Pu = null), Error(M(185)));
  ks(e, n, r),
    (!(K & 2) || e !== Ee) &&
      (e === Ee && (!(K & 2) && (ma |= n), Se === 4 && Sn(e, Ae)),
      Xe(e, r),
      n === 1 && K === 0 && !(t.mode & 1) && ((ai = me() + 500), da && Hn()));
}
function Xe(e, t) {
  var n = e.callbackNode;
  G1(e, t);
  var r = Ro(e, e === Ee ? Ae : 0);
  if (r === 0)
    n !== null && of(n), (e.callbackNode = null), (e.callbackPriority = 0);
  else if (((t = r & -r), e.callbackPriority !== t)) {
    if ((n != null && of(n), t === 1))
      e.tag === 0 ? Qx(Zf.bind(null, e)) : rg(Zf.bind(null, e)),
        $x(function () {
          !(K & 6) && Hn();
        }),
        (n = null);
    else {
      switch (bm(r)) {
        case 1:
          n = lc;
          break;
        case 4:
          n = Mm;
          break;
        case 16:
          n = Ao;
          break;
        case 536870912:
          n = Dm;
          break;
        default:
          n = Ao;
      }
      n = ty(n, Gg.bind(null, e));
    }
    (e.callbackPriority = t), (e.callbackNode = n);
  }
}
function Gg(e, t) {
  if (((go = -1), (yo = 0), K & 6)) throw Error(M(327));
  var n = e.callbackNode;
  if (Wr() && e.callbackNode !== n) return null;
  var r = Ro(e, e === Ee ? Ae : 0);
  if (r === 0) return null;
  if (r & 30 || r & e.expiredLanes || t) t = Ko(e, r);
  else {
    t = r;
    var i = K;
    K |= 2;
    var s = Xg();
    (Ee !== e || Ae !== t) && ((Qt = null), (ai = me() + 500), lr(e, t));
    do
      try {
        pw();
        break;
      } catch (a) {
        qg(e, a);
      }
    while (!0);
    Sc(),
      ($o.current = s),
      (K = i),
      ve !== null ? (t = 0) : ((Ee = null), (Ae = 0), (t = Se));
  }
  if (t !== 0) {
    if (
      (t === 2 && ((i = ql(e)), i !== 0 && ((r = i), (t = Cu(e, i)))), t === 1)
    )
      throw ((n = fs), lr(e, 0), Sn(e, r), Xe(e, me()), n);
    if (t === 6) Sn(e, r);
    else {
      if (
        ((i = e.current.alternate),
        !(r & 30) &&
          !fw(i) &&
          ((t = Ko(e, r)),
          t === 2 && ((s = ql(e)), s !== 0 && ((r = s), (t = Cu(e, s)))),
          t === 1))
      )
        throw ((n = fs), lr(e, 0), Sn(e, r), Xe(e, me()), n);
      switch (((e.finishedWork = i), (e.finishedLanes = r), t)) {
        case 0:
        case 1:
          throw Error(M(345));
        case 2:
          Xn(e, Ke, Qt);
          break;
        case 3:
          if (
            (Sn(e, r), (r & 130023424) === r && ((t = Ic + 500 - me()), 10 < t))
          ) {
            if (Ro(e, 0) !== 0) break;
            if (((i = e.suspendedLanes), (i & r) !== r)) {
              $e(), (e.pingedLanes |= e.suspendedLanes & i);
              break;
            }
            e.timeoutHandle = ru(Xn.bind(null, e, Ke, Qt), t);
            break;
          }
          Xn(e, Ke, Qt);
          break;
        case 4:
          if ((Sn(e, r), (r & 4194240) === r)) break;
          for (t = e.eventTimes, i = -1; 0 < r; ) {
            var o = 31 - kt(r);
            (s = 1 << o), (o = t[o]), o > i && (i = o), (r &= ~s);
          }
          if (
            ((r = i),
            (r = me() - r),
            (r =
              (120 > r
                ? 120
                : 480 > r
                ? 480
                : 1080 > r
                ? 1080
                : 1920 > r
                ? 1920
                : 3e3 > r
                ? 3e3
                : 4320 > r
                ? 4320
                : 1960 * dw(r / 1960)) - r),
            10 < r)
          ) {
            e.timeoutHandle = ru(Xn.bind(null, e, Ke, Qt), r);
            break;
          }
          Xn(e, Ke, Qt);
          break;
        case 5:
          Xn(e, Ke, Qt);
          break;
        default:
          throw Error(M(329));
      }
    }
  }
  return Xe(e, me()), e.callbackNode === n ? Gg.bind(null, e) : null;
}
function Cu(e, t) {
  var n = $i;
  return (
    e.current.memoizedState.isDehydrated && (lr(e, t).flags |= 256),
    (e = Ko(e, t)),
    e !== 2 && ((t = Ke), (Ke = n), t !== null && Eu(t)),
    e
  );
}
function Eu(e) {
  Ke === null ? (Ke = e) : Ke.push.apply(Ke, e);
}
function fw(e) {
  for (var t = e; ; ) {
    if (t.flags & 16384) {
      var n = t.updateQueue;
      if (n !== null && ((n = n.stores), n !== null))
        for (var r = 0; r < n.length; r++) {
          var i = n[r],
            s = i.getSnapshot;
          i = i.value;
          try {
            if (!Mt(s(), i)) return !1;
          } catch {
            return !1;
          }
        }
    }
    if (((n = t.child), t.subtreeFlags & 16384 && n !== null))
      (n.return = t), (t = n);
    else {
      if (t === e) break;
      for (; t.sibling === null; ) {
        if (t.return === null || t.return === e) return !0;
        t = t.return;
      }
      (t.sibling.return = t.return), (t = t.sibling);
    }
  }
  return !0;
}
function Sn(e, t) {
  for (
    t &= ~jc,
      t &= ~ma,
      e.suspendedLanes |= t,
      e.pingedLanes &= ~t,
      e = e.expirationTimes;
    0 < t;

  ) {
    var n = 31 - kt(t),
      r = 1 << n;
    (e[n] = -1), (t &= ~r);
  }
}
function Zf(e) {
  if (K & 6) throw Error(M(327));
  Wr();
  var t = Ro(e, 0);
  if (!(t & 1)) return Xe(e, me()), null;
  var n = Ko(e, t);
  if (e.tag !== 0 && n === 2) {
    var r = ql(e);
    r !== 0 && ((t = r), (n = Cu(e, r)));
  }
  if (n === 1) throw ((n = fs), lr(e, 0), Sn(e, t), Xe(e, me()), n);
  if (n === 6) throw Error(M(345));
  return (
    (e.finishedWork = e.current.alternate),
    (e.finishedLanes = t),
    Xn(e, Ke, Qt),
    Xe(e, me()),
    null
  );
}
function Fc(e, t) {
  var n = K;
  K |= 1;
  try {
    return e(t);
  } finally {
    (K = n), K === 0 && ((ai = me() + 500), da && Hn());
  }
}
function mr(e) {
  Rn !== null && Rn.tag === 0 && !(K & 6) && Wr();
  var t = K;
  K |= 1;
  var n = mt.transition,
    r = X;
  try {
    if (((mt.transition = null), (X = 1), e)) return e();
  } finally {
    (X = r), (mt.transition = n), (K = t), !(K & 6) && Hn();
  }
}
function _c() {
  (Je = Lr.current), re(Lr);
}
function lr(e, t) {
  (e.finishedWork = null), (e.finishedLanes = 0);
  var n = e.timeoutHandle;
  if ((n !== -1 && ((e.timeoutHandle = -1), Ux(n)), ve !== null))
    for (n = ve.return; n !== null; ) {
      var r = n;
      switch ((vc(r), r.tag)) {
        case 1:
          (r = r.type.childContextTypes), r != null && Lo();
          break;
        case 3:
          si(), re(Ge), re(Fe), Ac();
          break;
        case 5:
          kc(r);
          break;
        case 4:
          si();
          break;
        case 13:
          re(oe);
          break;
        case 19:
          re(oe);
          break;
        case 10:
          Pc(r.type._context);
          break;
        case 22:
        case 23:
          _c();
      }
      n = n.return;
    }
  if (
    ((Ee = e),
    (ve = e = In(e.current, null)),
    (Ae = Je = t),
    (Se = 0),
    (fs = null),
    (jc = ma = pr = 0),
    (Ke = $i = null),
    er !== null)
  ) {
    for (t = 0; t < er.length; t++)
      if (((n = er[t]), (r = n.interleaved), r !== null)) {
        n.interleaved = null;
        var i = r.next,
          s = n.pending;
        if (s !== null) {
          var o = s.next;
          (s.next = i), (r.next = o);
        }
        n.pending = r;
      }
    er = null;
  }
  return e;
}
function qg(e, t) {
  do {
    var n = ve;
    try {
      if ((Sc(), (ho.current = Uo), Bo)) {
        for (var r = ue.memoizedState; r !== null; ) {
          var i = r.queue;
          i !== null && (i.pending = null), (r = r.next);
        }
        Bo = !1;
      }
      if (
        ((hr = 0),
        (Ce = we = ue = null),
        (Bi = !1),
        (us = 0),
        (Oc.current = null),
        n === null || n.return === null)
      ) {
        (Se = 1), (fs = t), (ve = null);
        break;
      }
      e: {
        var s = e,
          o = n.return,
          a = n,
          l = t;
        if (
          ((t = Ae),
          (a.flags |= 32768),
          l !== null && typeof l == "object" && typeof l.then == "function")
        ) {
          var u = l,
            c = a,
            d = c.tag;
          if (!(c.mode & 1) && (d === 0 || d === 11 || d === 15)) {
            var f = c.alternate;
            f
              ? ((c.updateQueue = f.updateQueue),
                (c.memoizedState = f.memoizedState),
                (c.lanes = f.lanes))
              : ((c.updateQueue = null), (c.memoizedState = null));
          }
          var v = Vf(o);
          if (v !== null) {
            (v.flags &= -257),
              zf(v, o, a, s, t),
              v.mode & 1 && _f(s, u, t),
              (t = v),
              (l = u);
            var y = t.updateQueue;
            if (y === null) {
              var m = new Set();
              m.add(l), (t.updateQueue = m);
            } else y.add(l);
            break e;
          } else {
            if (!(t & 1)) {
              _f(s, u, t), Vc();
              break e;
            }
            l = Error(M(426));
          }
        } else if (ie && a.mode & 1) {
          var x = Vf(o);
          if (x !== null) {
            !(x.flags & 65536) && (x.flags |= 256),
              zf(x, o, a, s, t),
              xc(oi(l, a));
            break e;
          }
        }
        (s = l = oi(l, a)),
          Se !== 4 && (Se = 2),
          $i === null ? ($i = [s]) : $i.push(s),
          (s = o);
        do {
          switch (s.tag) {
            case 3:
              (s.flags |= 65536), (t &= -t), (s.lanes |= t);
              var h = bg(s, l, t);
              bf(s, h);
              break e;
            case 1:
              a = l;
              var p = s.type,
                g = s.stateNode;
              if (
                !(s.flags & 128) &&
                (typeof p.getDerivedStateFromError == "function" ||
                  (g !== null &&
                    typeof g.componentDidCatch == "function" &&
                    (On === null || !On.has(g))))
              ) {
                (s.flags |= 65536), (t &= -t), (s.lanes |= t);
                var S = Lg(s, a, t);
                bf(s, S);
                break e;
              }
          }
          s = s.return;
        } while (s !== null);
      }
      Zg(n);
    } catch (C) {
      (t = C), ve === n && n !== null && (ve = n = n.return);
      continue;
    }
    break;
  } while (!0);
}
function Xg() {
  var e = $o.current;
  return ($o.current = Uo), e === null ? Uo : e;
}
function Vc() {
  (Se === 0 || Se === 3 || Se === 2) && (Se = 4),
    Ee === null || (!(pr & 268435455) && !(ma & 268435455)) || Sn(Ee, Ae);
}
function Ko(e, t) {
  var n = K;
  K |= 2;
  var r = Xg();
  (Ee !== e || Ae !== t) && ((Qt = null), lr(e, t));
  do
    try {
      hw();
      break;
    } catch (i) {
      qg(e, i);
    }
  while (!0);
  if ((Sc(), (K = n), ($o.current = r), ve !== null)) throw Error(M(261));
  return (Ee = null), (Ae = 0), Se;
}
function hw() {
  for (; ve !== null; ) Yg(ve);
}
function pw() {
  for (; ve !== null && !V1(); ) Yg(ve);
}
function Yg(e) {
  var t = ey(e.alternate, e, Je);
  (e.memoizedProps = e.pendingProps),
    t === null ? Zg(e) : (ve = t),
    (Oc.current = null);
}
function Zg(e) {
  var t = e;
  do {
    var n = t.alternate;
    if (((e = t.return), t.flags & 32768)) {
      if (((n = aw(n, t)), n !== null)) {
        (n.flags &= 32767), (ve = n);
        return;
      }
      if (e !== null)
        (e.flags |= 32768), (e.subtreeFlags = 0), (e.deletions = null);
      else {
        (Se = 6), (ve = null);
        return;
      }
    } else if (((n = ow(n, t, Je)), n !== null)) {
      ve = n;
      return;
    }
    if (((t = t.sibling), t !== null)) {
      ve = t;
      return;
    }
    ve = t = e;
  } while (t !== null);
  Se === 0 && (Se = 5);
}
function Xn(e, t, n) {
  var r = X,
    i = mt.transition;
  try {
    (mt.transition = null), (X = 1), mw(e, t, n, r);
  } finally {
    (mt.transition = i), (X = r);
  }
  return null;
}
function mw(e, t, n, r) {
  do Wr();
  while (Rn !== null);
  if (K & 6) throw Error(M(327));
  n = e.finishedWork;
  var i = e.finishedLanes;
  if (n === null) return null;
  if (((e.finishedWork = null), (e.finishedLanes = 0), n === e.current))
    throw Error(M(177));
  (e.callbackNode = null), (e.callbackPriority = 0);
  var s = n.lanes | n.childLanes;
  if (
    (q1(e, s),
    e === Ee && ((ve = Ee = null), (Ae = 0)),
    (!(n.subtreeFlags & 2064) && !(n.flags & 2064)) ||
      Zs ||
      ((Zs = !0),
      ty(Ao, function () {
        return Wr(), null;
      })),
    (s = (n.flags & 15990) !== 0),
    n.subtreeFlags & 15990 || s)
  ) {
    (s = mt.transition), (mt.transition = null);
    var o = X;
    X = 1;
    var a = K;
    (K |= 4),
      (Oc.current = null),
      uw(e, n),
      Kg(n, e),
      jx(tu),
      (Mo = !!eu),
      (tu = eu = null),
      (e.current = n),
      cw(n),
      z1(),
      (K = a),
      (X = o),
      (mt.transition = s);
  } else e.current = n;
  if (
    (Zs && ((Zs = !1), (Rn = e), (Ho = i)),
    (s = e.pendingLanes),
    s === 0 && (On = null),
    $1(n.stateNode),
    Xe(e, me()),
    t !== null)
  )
    for (r = e.onRecoverableError, n = 0; n < t.length; n++)
      (i = t[n]), r(i.value, { componentStack: i.stack, digest: i.digest });
  if (Wo) throw ((Wo = !1), (e = Su), (Su = null), e);
  return (
    Ho & 1 && e.tag !== 0 && Wr(),
    (s = e.pendingLanes),
    s & 1 ? (e === Pu ? Wi++ : ((Wi = 0), (Pu = e))) : (Wi = 0),
    Hn(),
    null
  );
}
function Wr() {
  if (Rn !== null) {
    var e = bm(Ho),
      t = mt.transition,
      n = X;
    try {
      if (((mt.transition = null), (X = 16 > e ? 16 : e), Rn === null))
        var r = !1;
      else {
        if (((e = Rn), (Rn = null), (Ho = 0), K & 6)) throw Error(M(331));
        var i = K;
        for (K |= 4, O = e.current; O !== null; ) {
          var s = O,
            o = s.child;
          if (O.flags & 16) {
            var a = s.deletions;
            if (a !== null) {
              for (var l = 0; l < a.length; l++) {
                var u = a[l];
                for (O = u; O !== null; ) {
                  var c = O;
                  switch (c.tag) {
                    case 0:
                    case 11:
                    case 15:
                      Ui(8, c, s);
                  }
                  var d = c.child;
                  if (d !== null) (d.return = c), (O = d);
                  else
                    for (; O !== null; ) {
                      c = O;
                      var f = c.sibling,
                        v = c.return;
                      if (($g(c), c === u)) {
                        O = null;
                        break;
                      }
                      if (f !== null) {
                        (f.return = v), (O = f);
                        break;
                      }
                      O = v;
                    }
                }
              }
              var y = s.alternate;
              if (y !== null) {
                var m = y.child;
                if (m !== null) {
                  y.child = null;
                  do {
                    var x = m.sibling;
                    (m.sibling = null), (m = x);
                  } while (m !== null);
                }
              }
              O = s;
            }
          }
          if (s.subtreeFlags & 2064 && o !== null) (o.return = s), (O = o);
          else
            e: for (; O !== null; ) {
              if (((s = O), s.flags & 2048))
                switch (s.tag) {
                  case 0:
                  case 11:
                  case 15:
                    Ui(9, s, s.return);
                }
              var h = s.sibling;
              if (h !== null) {
                (h.return = s.return), (O = h);
                break e;
              }
              O = s.return;
            }
        }
        var p = e.current;
        for (O = p; O !== null; ) {
          o = O;
          var g = o.child;
          if (o.subtreeFlags & 2064 && g !== null) (g.return = o), (O = g);
          else
            e: for (o = p; O !== null; ) {
              if (((a = O), a.flags & 2048))
                try {
                  switch (a.tag) {
                    case 0:
                    case 11:
                    case 15:
                      pa(9, a);
                  }
                } catch (C) {
                  he(a, a.return, C);
                }
              if (a === o) {
                O = null;
                break e;
              }
              var S = a.sibling;
              if (S !== null) {
                (S.return = a.return), (O = S);
                break e;
              }
              O = a.return;
            }
        }
        if (
          ((K = i), Hn(), Ft && typeof Ft.onPostCommitFiberRoot == "function")
        )
          try {
            Ft.onPostCommitFiberRoot(oa, e);
          } catch {}
        r = !0;
      }
      return r;
    } finally {
      (X = n), (mt.transition = t);
    }
  }
  return !1;
}
function Jf(e, t, n) {
  (t = oi(n, t)),
    (t = bg(e, t, 1)),
    (e = Ln(e, t, 1)),
    (t = $e()),
    e !== null && (ks(e, 1, t), Xe(e, t));
}
function he(e, t, n) {
  if (e.tag === 3) Jf(e, e, n);
  else
    for (; t !== null; ) {
      if (t.tag === 3) {
        Jf(t, e, n);
        break;
      } else if (t.tag === 1) {
        var r = t.stateNode;
        if (
          typeof t.type.getDerivedStateFromError == "function" ||
          (typeof r.componentDidCatch == "function" &&
            (On === null || !On.has(r)))
        ) {
          (e = oi(n, e)),
            (e = Lg(t, e, 1)),
            (t = Ln(t, e, 1)),
            (e = $e()),
            t !== null && (ks(t, 1, e), Xe(t, e));
          break;
        }
      }
      t = t.return;
    }
}
function gw(e, t, n) {
  var r = e.pingCache;
  r !== null && r.delete(t),
    (t = $e()),
    (e.pingedLanes |= e.suspendedLanes & n),
    Ee === e &&
      (Ae & n) === n &&
      (Se === 4 || (Se === 3 && (Ae & 130023424) === Ae && 500 > me() - Ic)
        ? lr(e, 0)
        : (jc |= n)),
    Xe(e, t);
}
function Jg(e, t) {
  t === 0 &&
    (e.mode & 1
      ? ((t = Us), (Us <<= 1), !(Us & 130023424) && (Us = 4194304))
      : (t = 1));
  var n = $e();
  (e = rn(e, t)), e !== null && (ks(e, t, n), Xe(e, n));
}
function yw(e) {
  var t = e.memoizedState,
    n = 0;
  t !== null && (n = t.retryLane), Jg(e, n);
}
function vw(e, t) {
  var n = 0;
  switch (e.tag) {
    case 13:
      var r = e.stateNode,
        i = e.memoizedState;
      i !== null && (n = i.retryLane);
      break;
    case 19:
      r = e.stateNode;
      break;
    default:
      throw Error(M(314));
  }
  r !== null && r.delete(t), Jg(e, n);
}
var ey;
ey = function (e, t, n) {
  if (e !== null)
    if (e.memoizedProps !== t.pendingProps || Ge.current) Qe = !0;
    else {
      if (!(e.lanes & n) && !(t.flags & 128)) return (Qe = !1), sw(e, t, n);
      Qe = !!(e.flags & 131072);
    }
  else (Qe = !1), ie && t.flags & 1048576 && ig(t, Io, t.index);
  switch (((t.lanes = 0), t.tag)) {
    case 2:
      var r = t.type;
      mo(e, t), (e = t.pendingProps);
      var i = ni(t, Fe.current);
      $r(t, n), (i = Mc(null, t, r, e, i, n));
      var s = Dc();
      return (
        (t.flags |= 1),
        typeof i == "object" &&
        i !== null &&
        typeof i.render == "function" &&
        i.$$typeof === void 0
          ? ((t.tag = 1),
            (t.memoizedState = null),
            (t.updateQueue = null),
            qe(r) ? ((s = !0), Oo(t)) : (s = !1),
            (t.memoizedState =
              i.state !== null && i.state !== void 0 ? i.state : null),
            Ec(t),
            (i.updater = ha),
            (t.stateNode = i),
            (i._reactInternals = t),
            cu(t, r, e, n),
            (t = hu(null, t, r, !0, s, n)))
          : ((t.tag = 0), ie && s && yc(t), Be(null, t, i, n), (t = t.child)),
        t
      );
    case 16:
      r = t.elementType;
      e: {
        switch (
          (mo(e, t),
          (e = t.pendingProps),
          (i = r._init),
          (r = i(r._payload)),
          (t.type = r),
          (i = t.tag = ww(r)),
          (e = St(r, e)),
          i)
        ) {
          case 0:
            t = fu(null, t, r, e, n);
            break e;
          case 1:
            t = $f(null, t, r, e, n);
            break e;
          case 11:
            t = Bf(null, t, r, e, n);
            break e;
          case 14:
            t = Uf(null, t, r, St(r.type, e), n);
            break e;
        }
        throw Error(M(306, r, ""));
      }
      return t;
    case 0:
      return (
        (r = t.type),
        (i = t.pendingProps),
        (i = t.elementType === r ? i : St(r, i)),
        fu(e, t, r, i, n)
      );
    case 1:
      return (
        (r = t.type),
        (i = t.pendingProps),
        (i = t.elementType === r ? i : St(r, i)),
        $f(e, t, r, i, n)
      );
    case 3:
      e: {
        if ((Fg(t), e === null)) throw Error(M(387));
        (r = t.pendingProps),
          (s = t.memoizedState),
          (i = s.element),
          cg(e, t),
          Vo(t, r, null, n);
        var o = t.memoizedState;
        if (((r = o.element), s.isDehydrated))
          if (
            ((s = {
              element: r,
              isDehydrated: !1,
              cache: o.cache,
              pendingSuspenseBoundaries: o.pendingSuspenseBoundaries,
              transitions: o.transitions,
            }),
            (t.updateQueue.baseState = s),
            (t.memoizedState = s),
            t.flags & 256)
          ) {
            (i = oi(Error(M(423)), t)), (t = Wf(e, t, r, n, i));
            break e;
          } else if (r !== i) {
            (i = oi(Error(M(424)), t)), (t = Wf(e, t, r, n, i));
            break e;
          } else
            for (
              tt = bn(t.stateNode.containerInfo.firstChild),
                nt = t,
                ie = !0,
                Tt = null,
                n = lg(t, null, r, n),
                t.child = n;
              n;

            )
              (n.flags = (n.flags & -3) | 4096), (n = n.sibling);
        else {
          if ((ri(), r === i)) {
            t = sn(e, t, n);
            break e;
          }
          Be(e, t, r, n);
        }
        t = t.child;
      }
      return t;
    case 5:
      return (
        dg(t),
        e === null && au(t),
        (r = t.type),
        (i = t.pendingProps),
        (s = e !== null ? e.memoizedProps : null),
        (o = i.children),
        nu(r, i) ? (o = null) : s !== null && nu(r, s) && (t.flags |= 32),
        Ig(e, t),
        Be(e, t, o, n),
        t.child
      );
    case 6:
      return e === null && au(t), null;
    case 13:
      return _g(e, t, n);
    case 4:
      return (
        Tc(t, t.stateNode.containerInfo),
        (r = t.pendingProps),
        e === null ? (t.child = ii(t, null, r, n)) : Be(e, t, r, n),
        t.child
      );
    case 11:
      return (
        (r = t.type),
        (i = t.pendingProps),
        (i = t.elementType === r ? i : St(r, i)),
        Bf(e, t, r, i, n)
      );
    case 7:
      return Be(e, t, t.pendingProps, n), t.child;
    case 8:
      return Be(e, t, t.pendingProps.children, n), t.child;
    case 12:
      return Be(e, t, t.pendingProps.children, n), t.child;
    case 10:
      e: {
        if (
          ((r = t.type._context),
          (i = t.pendingProps),
          (s = t.memoizedProps),
          (o = i.value),
          ee(Fo, r._currentValue),
          (r._currentValue = o),
          s !== null)
        )
          if (Mt(s.value, o)) {
            if (s.children === i.children && !Ge.current) {
              t = sn(e, t, n);
              break e;
            }
          } else
            for (s = t.child, s !== null && (s.return = t); s !== null; ) {
              var a = s.dependencies;
              if (a !== null) {
                o = s.child;
                for (var l = a.firstContext; l !== null; ) {
                  if (l.context === r) {
                    if (s.tag === 1) {
                      (l = Zt(-1, n & -n)), (l.tag = 2);
                      var u = s.updateQueue;
                      if (u !== null) {
                        u = u.shared;
                        var c = u.pending;
                        c === null
                          ? (l.next = l)
                          : ((l.next = c.next), (c.next = l)),
                          (u.pending = l);
                      }
                    }
                    (s.lanes |= n),
                      (l = s.alternate),
                      l !== null && (l.lanes |= n),
                      lu(s.return, n, t),
                      (a.lanes |= n);
                    break;
                  }
                  l = l.next;
                }
              } else if (s.tag === 10) o = s.type === t.type ? null : s.child;
              else if (s.tag === 18) {
                if (((o = s.return), o === null)) throw Error(M(341));
                (o.lanes |= n),
                  (a = o.alternate),
                  a !== null && (a.lanes |= n),
                  lu(o, n, t),
                  (o = s.sibling);
              } else o = s.child;
              if (o !== null) o.return = s;
              else
                for (o = s; o !== null; ) {
                  if (o === t) {
                    o = null;
                    break;
                  }
                  if (((s = o.sibling), s !== null)) {
                    (s.return = o.return), (o = s);
                    break;
                  }
                  o = o.return;
                }
              s = o;
            }
        Be(e, t, i.children, n), (t = t.child);
      }
      return t;
    case 9:
      return (
        (i = t.type),
        (r = t.pendingProps.children),
        $r(t, n),
        (i = gt(i)),
        (r = r(i)),
        (t.flags |= 1),
        Be(e, t, r, n),
        t.child
      );
    case 14:
      return (
        (r = t.type),
        (i = St(r, t.pendingProps)),
        (i = St(r.type, i)),
        Uf(e, t, r, i, n)
      );
    case 15:
      return Og(e, t, t.type, t.pendingProps, n);
    case 17:
      return (
        (r = t.type),
        (i = t.pendingProps),
        (i = t.elementType === r ? i : St(r, i)),
        mo(e, t),
        (t.tag = 1),
        qe(r) ? ((e = !0), Oo(t)) : (e = !1),
        $r(t, n),
        Ng(t, r, i),
        cu(t, r, i, n),
        hu(null, t, r, !0, e, n)
      );
    case 19:
      return Vg(e, t, n);
    case 22:
      return jg(e, t, n);
  }
  throw Error(M(156, t.tag));
};
function ty(e, t) {
  return Rm(e, t);
}
function xw(e, t, n, r) {
  (this.tag = e),
    (this.key = n),
    (this.sibling =
      this.child =
      this.return =
      this.stateNode =
      this.type =
      this.elementType =
        null),
    (this.index = 0),
    (this.ref = null),
    (this.pendingProps = t),
    (this.dependencies =
      this.memoizedState =
      this.updateQueue =
      this.memoizedProps =
        null),
    (this.mode = r),
    (this.subtreeFlags = this.flags = 0),
    (this.deletions = null),
    (this.childLanes = this.lanes = 0),
    (this.alternate = null);
}
function pt(e, t, n, r) {
  return new xw(e, t, n, r);
}
function zc(e) {
  return (e = e.prototype), !(!e || !e.isReactComponent);
}
function ww(e) {
  if (typeof e == "function") return zc(e) ? 1 : 0;
  if (e != null) {
    if (((e = e.$$typeof), e === sc)) return 11;
    if (e === oc) return 14;
  }
  return 2;
}
function In(e, t) {
  var n = e.alternate;
  return (
    n === null
      ? ((n = pt(e.tag, t, e.key, e.mode)),
        (n.elementType = e.elementType),
        (n.type = e.type),
        (n.stateNode = e.stateNode),
        (n.alternate = e),
        (e.alternate = n))
      : ((n.pendingProps = t),
        (n.type = e.type),
        (n.flags = 0),
        (n.subtreeFlags = 0),
        (n.deletions = null)),
    (n.flags = e.flags & 14680064),
    (n.childLanes = e.childLanes),
    (n.lanes = e.lanes),
    (n.child = e.child),
    (n.memoizedProps = e.memoizedProps),
    (n.memoizedState = e.memoizedState),
    (n.updateQueue = e.updateQueue),
    (t = e.dependencies),
    (n.dependencies =
      t === null ? null : { lanes: t.lanes, firstContext: t.firstContext }),
    (n.sibling = e.sibling),
    (n.index = e.index),
    (n.ref = e.ref),
    n
  );
}
function vo(e, t, n, r, i, s) {
  var o = 2;
  if (((r = e), typeof e == "function")) zc(e) && (o = 1);
  else if (typeof e == "string") o = 5;
  else
    e: switch (e) {
      case Cr:
        return ur(n.children, i, s, t);
      case ic:
        (o = 8), (i |= 8);
        break;
      case Ol:
        return (
          (e = pt(12, n, t, i | 2)), (e.elementType = Ol), (e.lanes = s), e
        );
      case jl:
        return (e = pt(13, n, t, i)), (e.elementType = jl), (e.lanes = s), e;
      case Il:
        return (e = pt(19, n, t, i)), (e.elementType = Il), (e.lanes = s), e;
      case dm:
        return ga(n, i, s, t);
      default:
        if (typeof e == "object" && e !== null)
          switch (e.$$typeof) {
            case um:
              o = 10;
              break e;
            case cm:
              o = 9;
              break e;
            case sc:
              o = 11;
              break e;
            case oc:
              o = 14;
              break e;
            case vn:
              (o = 16), (r = null);
              break e;
          }
        throw Error(M(130, e == null ? e : typeof e, ""));
    }
  return (
    (t = pt(o, n, t, i)), (t.elementType = e), (t.type = r), (t.lanes = s), t
  );
}
function ur(e, t, n, r) {
  return (e = pt(7, e, r, t)), (e.lanes = n), e;
}
function ga(e, t, n, r) {
  return (
    (e = pt(22, e, r, t)),
    (e.elementType = dm),
    (e.lanes = n),
    (e.stateNode = { isHidden: !1 }),
    e
  );
}
function fl(e, t, n) {
  return (e = pt(6, e, null, t)), (e.lanes = n), e;
}
function hl(e, t, n) {
  return (
    (t = pt(4, e.children !== null ? e.children : [], e.key, t)),
    (t.lanes = n),
    (t.stateNode = {
      containerInfo: e.containerInfo,
      pendingChildren: null,
      implementation: e.implementation,
    }),
    t
  );
}
function Sw(e, t, n, r, i) {
  (this.tag = t),
    (this.containerInfo = e),
    (this.finishedWork =
      this.pingCache =
      this.current =
      this.pendingChildren =
        null),
    (this.timeoutHandle = -1),
    (this.callbackNode = this.pendingContext = this.context = null),
    (this.callbackPriority = 0),
    (this.eventTimes = Qa(0)),
    (this.expirationTimes = Qa(-1)),
    (this.entangledLanes =
      this.finishedLanes =
      this.mutableReadLanes =
      this.expiredLanes =
      this.pingedLanes =
      this.suspendedLanes =
      this.pendingLanes =
        0),
    (this.entanglements = Qa(0)),
    (this.identifierPrefix = r),
    (this.onRecoverableError = i),
    (this.mutableSourceEagerHydrationData = null);
}
function Bc(e, t, n, r, i, s, o, a, l) {
  return (
    (e = new Sw(e, t, n, a, l)),
    t === 1 ? ((t = 1), s === !0 && (t |= 8)) : (t = 0),
    (s = pt(3, null, null, t)),
    (e.current = s),
    (s.stateNode = e),
    (s.memoizedState = {
      element: r,
      isDehydrated: n,
      cache: null,
      transitions: null,
      pendingSuspenseBoundaries: null,
    }),
    Ec(s),
    e
  );
}
function Pw(e, t, n) {
  var r = 3 < arguments.length && arguments[3] !== void 0 ? arguments[3] : null;
  return {
    $$typeof: Pr,
    key: r == null ? null : "" + r,
    children: e,
    containerInfo: t,
    implementation: n,
  };
}
function ny(e) {
  if (!e) return zn;
  e = e._reactInternals;
  e: {
    if (xr(e) !== e || e.tag !== 1) throw Error(M(170));
    var t = e;
    do {
      switch (t.tag) {
        case 3:
          t = t.stateNode.context;
          break e;
        case 1:
          if (qe(t.type)) {
            t = t.stateNode.__reactInternalMemoizedMergedChildContext;
            break e;
          }
      }
      t = t.return;
    } while (t !== null);
    throw Error(M(171));
  }
  if (e.tag === 1) {
    var n = e.type;
    if (qe(n)) return ng(e, n, t);
  }
  return t;
}
function ry(e, t, n, r, i, s, o, a, l) {
  return (
    (e = Bc(n, r, !0, e, i, s, o, a, l)),
    (e.context = ny(null)),
    (n = e.current),
    (r = $e()),
    (i = jn(n)),
    (s = Zt(r, i)),
    (s.callback = t ?? null),
    Ln(n, s, i),
    (e.current.lanes = i),
    ks(e, i, r),
    Xe(e, r),
    e
  );
}
function ya(e, t, n, r) {
  var i = t.current,
    s = $e(),
    o = jn(i);
  return (
    (n = ny(n)),
    t.context === null ? (t.context = n) : (t.pendingContext = n),
    (t = Zt(s, o)),
    (t.payload = { element: e }),
    (r = r === void 0 ? null : r),
    r !== null && (t.callback = r),
    (e = Ln(i, t, o)),
    e !== null && (At(e, i, o, s), fo(e, i, o)),
    o
  );
}
function Qo(e) {
  if (((e = e.current), !e.child)) return null;
  switch (e.child.tag) {
    case 5:
      return e.child.stateNode;
    default:
      return e.child.stateNode;
  }
}
function eh(e, t) {
  if (((e = e.memoizedState), e !== null && e.dehydrated !== null)) {
    var n = e.retryLane;
    e.retryLane = n !== 0 && n < t ? n : t;
  }
}
function Uc(e, t) {
  eh(e, t), (e = e.alternate) && eh(e, t);
}
function Cw() {
  return null;
}
var iy =
  typeof reportError == "function"
    ? reportError
    : function (e) {
        console.error(e);
      };
function $c(e) {
  this._internalRoot = e;
}
va.prototype.render = $c.prototype.render = function (e) {
  var t = this._internalRoot;
  if (t === null) throw Error(M(409));
  ya(e, t, null, null);
};
va.prototype.unmount = $c.prototype.unmount = function () {
  var e = this._internalRoot;
  if (e !== null) {
    this._internalRoot = null;
    var t = e.containerInfo;
    mr(function () {
      ya(null, e, null, null);
    }),
      (t[nn] = null);
  }
};
function va(e) {
  this._internalRoot = e;
}
va.prototype.unstable_scheduleHydration = function (e) {
  if (e) {
    var t = jm();
    e = { blockedOn: null, target: e, priority: t };
    for (var n = 0; n < wn.length && t !== 0 && t < wn[n].priority; n++);
    wn.splice(n, 0, e), n === 0 && Fm(e);
  }
};
function Wc(e) {
  return !(!e || (e.nodeType !== 1 && e.nodeType !== 9 && e.nodeType !== 11));
}
function xa(e) {
  return !(
    !e ||
    (e.nodeType !== 1 &&
      e.nodeType !== 9 &&
      e.nodeType !== 11 &&
      (e.nodeType !== 8 || e.nodeValue !== " react-mount-point-unstable "))
  );
}
function th() {}
function Ew(e, t, n, r, i) {
  if (i) {
    if (typeof r == "function") {
      var s = r;
      r = function () {
        var u = Qo(o);
        s.call(u);
      };
    }
    var o = ry(t, r, e, 0, null, !1, !1, "", th);
    return (
      (e._reactRootContainer = o),
      (e[nn] = o.current),
      is(e.nodeType === 8 ? e.parentNode : e),
      mr(),
      o
    );
  }
  for (; (i = e.lastChild); ) e.removeChild(i);
  if (typeof r == "function") {
    var a = r;
    r = function () {
      var u = Qo(l);
      a.call(u);
    };
  }
  var l = Bc(e, 0, !1, null, null, !1, !1, "", th);
  return (
    (e._reactRootContainer = l),
    (e[nn] = l.current),
    is(e.nodeType === 8 ? e.parentNode : e),
    mr(function () {
      ya(t, l, n, r);
    }),
    l
  );
}
function wa(e, t, n, r, i) {
  var s = n._reactRootContainer;
  if (s) {
    var o = s;
    if (typeof i == "function") {
      var a = i;
      i = function () {
        var l = Qo(o);
        a.call(l);
      };
    }
    ya(t, o, e, i);
  } else o = Ew(n, t, e, i, r);
  return Qo(o);
}
Lm = function (e) {
  switch (e.tag) {
    case 3:
      var t = e.stateNode;
      if (t.current.memoizedState.isDehydrated) {
        var n = Ni(t.pendingLanes);
        n !== 0 &&
          (uc(t, n | 1), Xe(t, me()), !(K & 6) && ((ai = me() + 500), Hn()));
      }
      break;
    case 13:
      mr(function () {
        var r = rn(e, 1);
        if (r !== null) {
          var i = $e();
          At(r, e, 1, i);
        }
      }),
        Uc(e, 1);
  }
};
cc = function (e) {
  if (e.tag === 13) {
    var t = rn(e, 134217728);
    if (t !== null) {
      var n = $e();
      At(t, e, 134217728, n);
    }
    Uc(e, 134217728);
  }
};
Om = function (e) {
  if (e.tag === 13) {
    var t = jn(e),
      n = rn(e, t);
    if (n !== null) {
      var r = $e();
      At(n, e, t, r);
    }
    Uc(e, t);
  }
};
jm = function () {
  return X;
};
Im = function (e, t) {
  var n = X;
  try {
    return (X = e), t();
  } finally {
    X = n;
  }
};
Kl = function (e, t, n) {
  switch (t) {
    case "input":
      if ((Vl(e, n), (t = n.name), n.type === "radio" && t != null)) {
        for (n = e; n.parentNode; ) n = n.parentNode;
        for (
          n = n.querySelectorAll(
            "input[name=" + JSON.stringify("" + t) + '][type="radio"]'
          ),
            t = 0;
          t < n.length;
          t++
        ) {
          var r = n[t];
          if (r !== e && r.form === e.form) {
            var i = ca(r);
            if (!i) throw Error(M(90));
            hm(r), Vl(r, i);
          }
        }
      }
      break;
    case "textarea":
      mm(e, n);
      break;
    case "select":
      (t = n.value), t != null && Vr(e, !!n.multiple, t, !1);
  }
};
Pm = Fc;
Cm = mr;
var Tw = { usingClientEntryPoint: !1, Events: [Rs, Ar, ca, wm, Sm, Fc] },
  Ti = {
    findFiberByHostInstance: Jn,
    bundleType: 0,
    version: "18.3.1",
    rendererPackageName: "react-dom",
  },
  kw = {
    bundleType: Ti.bundleType,
    version: Ti.version,
    rendererPackageName: Ti.rendererPackageName,
    rendererConfig: Ti.rendererConfig,
    overrideHookState: null,
    overrideHookStateDeletePath: null,
    overrideHookStateRenamePath: null,
    overrideProps: null,
    overridePropsDeletePath: null,
    overridePropsRenamePath: null,
    setErrorHandler: null,
    setSuspenseHandler: null,
    scheduleUpdate: null,
    currentDispatcherRef: ln.ReactCurrentDispatcher,
    findHostInstanceByFiber: function (e) {
      return (e = km(e)), e === null ? null : e.stateNode;
    },
    findFiberByHostInstance: Ti.findFiberByHostInstance || Cw,
    findHostInstancesForRefresh: null,
    scheduleRefresh: null,
    scheduleRoot: null,
    setRefreshHandler: null,
    getCurrentFiber: null,
    reconcilerVersion: "18.3.1-next-f1338f8080-20240426",
  };
if (typeof __REACT_DEVTOOLS_GLOBAL_HOOK__ < "u") {
  var Js = __REACT_DEVTOOLS_GLOBAL_HOOK__;
  if (!Js.isDisabled && Js.supportsFiber)
    try {
      (oa = Js.inject(kw)), (Ft = Js);
    } catch {}
}
st.__SECRET_INTERNALS_DO_NOT_USE_OR_YOU_WILL_BE_FIRED = Tw;
st.createPortal = function (e, t) {
  var n = 2 < arguments.length && arguments[2] !== void 0 ? arguments[2] : null;
  if (!Wc(t)) throw Error(M(200));
  return Pw(e, t, null, n);
};
st.createRoot = function (e, t) {
  if (!Wc(e)) throw Error(M(299));
  var n = !1,
    r = "",
    i = iy;
  return (
    t != null &&
      (t.unstable_strictMode === !0 && (n = !0),
      t.identifierPrefix !== void 0 && (r = t.identifierPrefix),
      t.onRecoverableError !== void 0 && (i = t.onRecoverableError)),
    (t = Bc(e, 1, !1, null, null, n, !1, r, i)),
    (e[nn] = t.current),
    is(e.nodeType === 8 ? e.parentNode : e),
    new $c(t)
  );
};
st.findDOMNode = function (e) {
  if (e == null) return null;
  if (e.nodeType === 1) return e;
  var t = e._reactInternals;
  if (t === void 0)
    throw typeof e.render == "function"
      ? Error(M(188))
      : ((e = Object.keys(e).join(",")), Error(M(268, e)));
  return (e = km(t)), (e = e === null ? null : e.stateNode), e;
};
st.flushSync = function (e) {
  return mr(e);
};
st.hydrate = function (e, t, n) {
  if (!xa(t)) throw Error(M(200));
  return wa(null, e, t, !0, n);
};
st.hydrateRoot = function (e, t, n) {
  if (!Wc(e)) throw Error(M(405));
  var r = (n != null && n.hydratedSources) || null,
    i = !1,
    s = "",
    o = iy;
  if (
    (n != null &&
      (n.unstable_strictMode === !0 && (i = !0),
      n.identifierPrefix !== void 0 && (s = n.identifierPrefix),
      n.onRecoverableError !== void 0 && (o = n.onRecoverableError)),
    (t = ry(t, null, e, 1, n ?? null, i, !1, s, o)),
    (e[nn] = t.current),
    is(e),
    r)
  )
    for (e = 0; e < r.length; e++)
      (n = r[e]),
        (i = n._getVersion),
        (i = i(n._source)),
        t.mutableSourceEagerHydrationData == null
          ? (t.mutableSourceEagerHydrationData = [n, i])
          : t.mutableSourceEagerHydrationData.push(n, i);
  return new va(t);
};
st.render = function (e, t, n) {
  if (!xa(t)) throw Error(M(200));
  return wa(null, e, t, !1, n);
};
st.unmountComponentAtNode = function (e) {
  if (!xa(e)) throw Error(M(40));
  return e._reactRootContainer
    ? (mr(function () {
        wa(null, null, e, !1, function () {
          (e._reactRootContainer = null), (e[nn] = null);
        });
      }),
      !0)
    : !1;
};
st.unstable_batchedUpdates = Fc;
st.unstable_renderSubtreeIntoContainer = function (e, t, n, r) {
  if (!xa(n)) throw Error(M(200));
  if (e == null || e._reactInternals === void 0) throw Error(M(38));
  return wa(e, t, n, !1, r);
};
st.version = "18.3.1-next-f1338f8080-20240426";
function sy() {
  if (
    !(
      typeof __REACT_DEVTOOLS_GLOBAL_HOOK__ > "u" ||
      typeof __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE != "function"
    )
  )
    try {
      __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE(sy);
    } catch (e) {
      console.error(e);
    }
}
sy(), (sm.exports = st);
var Sa = sm.exports;
const Aw = Qp(Sa);
var oy,
  nh = Sa;
(oy = nh.createRoot), nh.hydrateRoot;
function Rw(e, t) {
  if (e instanceof RegExp) return { keys: !1, pattern: e };
  var n,
    r,
    i,
    s,
    o = [],
    a = "",
    l = e.split("/");
  for (l[0] || l.shift(); (i = l.shift()); )
    (n = i[0]),
      n === "*"
        ? (o.push(n), (a += i[1] === "?" ? "(?:/(.*))?" : "/(.*)"))
        : n === ":"
        ? ((r = i.indexOf("?", 1)),
          (s = i.indexOf(".", 1)),
          o.push(i.substring(1, ~r ? r : ~s ? s : i.length)),
          (a += ~r && !~s ? "(?:/([^/]+?))?" : "/([^/]+?)"),
          ~s && (a += (~r ? "?" : "") + "\\" + i.substring(s)))
        : (a += "/" + i);
  return {
    keys: o,
    pattern: new RegExp("^" + a + (t ? "(?=$|/)" : "/?$"), "i"),
  };
}
var ay = { exports: {} },
  ly = {};
/**
 * @license React
 * use-sync-external-store-shim.production.min.js
 *
 * Copyright (c) Facebook, Inc. and its affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */ var li = w;
function Mw(e, t) {
  return (e === t && (e !== 0 || 1 / e === 1 / t)) || (e !== e && t !== t);
}
var Dw = typeof Object.is == "function" ? Object.is : Mw,
  Nw = li.useState,
  bw = li.useEffect,
  Lw = li.useLayoutEffect,
  Ow = li.useDebugValue;
function jw(e, t) {
  var n = t(),
    r = Nw({ inst: { value: n, getSnapshot: t } }),
    i = r[0].inst,
    s = r[1];
  return (
    Lw(
      function () {
        (i.value = n), (i.getSnapshot = t), pl(i) && s({ inst: i });
      },
      [e, n, t]
    ),
    bw(
      function () {
        return (
          pl(i) && s({ inst: i }),
          e(function () {
            pl(i) && s({ inst: i });
          })
        );
      },
      [e]
    ),
    Ow(n),
    n
  );
}
function pl(e) {
  var t = e.getSnapshot;
  e = e.value;
  try {
    var n = t();
    return !Dw(e, n);
  } catch {
    return !0;
  }
}
function Iw(e, t) {
  return t();
}
var Fw =
  typeof window > "u" ||
  typeof window.document > "u" ||
  typeof window.document.createElement > "u"
    ? Iw
    : jw;
ly.useSyncExternalStore =
  li.useSyncExternalStore !== void 0 ? li.useSyncExternalStore : Fw;
ay.exports = ly;
var _w = ay.exports;
const Vw = g1.useInsertionEffect,
  zw =
    typeof window < "u" &&
    typeof window.document < "u" &&
    typeof window.document.createElement < "u",
  Bw = zw ? w.useLayoutEffect : w.useEffect,
  Uw = Vw || Bw,
  uy = (e) => {
    const t = w.useRef([e, (...n) => t[0](...n)]).current;
    return (
      Uw(() => {
        t[0] = e;
      }),
      t[1]
    );
  },
  $w = "popstate",
  Hc = "pushState",
  Kc = "replaceState",
  Ww = "hashchange",
  rh = [$w, Hc, Kc, Ww],
  Hw = (e) => {
    for (const t of rh) addEventListener(t, e);
    return () => {
      for (const t of rh) removeEventListener(t, e);
    };
  },
  cy = (e, t) => _w.useSyncExternalStore(Hw, e, t),
  Kw = () => location.search,
  Qw = ({ ssrSearch: e = "" } = {}) => cy(Kw, () => e),
  ih = () => location.pathname,
  Gw = ({ ssrPath: e } = {}) => cy(ih, e ? () => e : ih),
  qw = (e, { replace: t = !1, state: n = null } = {}) =>
    history[t ? Kc : Hc](n, "", e),
  Xw = (e = {}) => [Gw(e), qw],
  sh = Symbol.for("wouter_v3");
if (typeof history < "u" && typeof window[sh] > "u") {
  for (const e of [Hc, Kc]) {
    const t = history[e];
    history[e] = function () {
      const n = t.apply(this, arguments),
        r = new Event(e);
      return (r.arguments = arguments), dispatchEvent(r), n;
    };
  }
  Object.defineProperty(window, sh, { value: !0 });
}
const Yw = (e, t) =>
    t.toLowerCase().indexOf(e.toLowerCase())
      ? "~" + t
      : t.slice(e.length) || "/",
  dy = (e = "") => (e === "/" ? "" : e),
  Zw = (e, t) => (e[0] === "~" ? e.slice(1) : dy(t) + e),
  Jw = (e = "", t) => Yw(oh(dy(e)), oh(t)),
  oh = (e) => {
    try {
      return decodeURI(e);
    } catch {
      return e;
    }
  },
  fy = {
    hook: Xw,
    searchHook: Qw,
    parser: Rw,
    base: "",
    ssrPath: void 0,
    ssrSearch: void 0,
    hrefs: (e) => e,
  },
  hy = w.createContext(fy),
  Pa = () => w.useContext(hy),
  py = {},
  my = w.createContext(py),
  eS = () => w.useContext(my),
  Qc = (e) => {
    const [t, n] = e.hook(e);
    return [Jw(e.base, t), uy((r, i) => n(Zw(r, e.base), i))];
  },
  gy = (e, t, n, r) => {
    const { pattern: i, keys: s } =
        t instanceof RegExp ? { keys: !1, pattern: t } : e(t || "*", r),
      o = i.exec(n) || [],
      [a, ...l] = o;
    return a !== void 0
      ? [
          !0,
          (() => {
            const u =
              s !== !1
                ? Object.fromEntries(s.map((d, f) => [d, l[f]]))
                : o.groups;
            let c = { ...l };
            return u && Object.assign(c, u), c;
          })(),
          ...(r ? [a] : []),
        ]
      : [!1, null];
  },
  tS = ({ children: e, ...t }) => {
    var c, d;
    const n = Pa(),
      r = t.hook ? fy : n;
    let i = r;
    const [s, o] = ((c = t.ssrPath) == null ? void 0 : c.split("?")) ?? [];
    o && ((t.ssrSearch = o), (t.ssrPath = s)),
      (t.hrefs = t.hrefs ?? ((d = t.hook) == null ? void 0 : d.hrefs));
    let a = w.useRef({}),
      l = a.current,
      u = l;
    for (let f in r) {
      const v = f === "base" ? r[f] + (t[f] || "") : t[f] || r[f];
      l === u && v !== u[f] && (a.current = u = { ...u }),
        (u[f] = v),
        v !== r[f] && (i = u);
    }
    return w.createElement(hy.Provider, { value: i, children: e });
  },
  ah = ({ children: e, component: t }, n) =>
    t ? w.createElement(t, { params: n }) : typeof e == "function" ? e(n) : e,
  nS = (e) => {
    let t = w.useRef(py),
      n = t.current;
    for (const r in e) e[r] !== n[r] && (n = e);
    return Object.keys(e).length === 0 && (n = e), (t.current = n);
  },
  lh = ({ path: e, nest: t, match: n, ...r }) => {
    const i = Pa(),
      [s] = Qc(i),
      [o, a, l] = n ?? gy(i.parser, e, s, t),
      u = nS({ ...eS(), ...a });
    if (!o) return null;
    const c = l ? w.createElement(tS, { base: l }, ah(r, u)) : ah(r, u);
    return w.createElement(my.Provider, { value: u, children: c });
  },
  rS = w.forwardRef((e, t) => {
    const n = Pa(),
      [r, i] = Qc(n),
      {
        to: s = "",
        href: o = s,
        onClick: a,
        asChild: l,
        children: u,
        className: c,
        replace: d,
        state: f,
        ...v
      } = e,
      y = uy((x) => {
        x.ctrlKey ||
          x.metaKey ||
          x.altKey ||
          x.shiftKey ||
          x.button !== 0 ||
          (a == null || a(x),
          x.defaultPrevented || (x.preventDefault(), i(o, e)));
      }),
      m = n.hrefs(o[0] === "~" ? o.slice(1) : n.base + o, n);
    return l && w.isValidElement(u)
      ? w.cloneElement(u, { onClick: y, href: m })
      : w.createElement("a", {
          ...v,
          onClick: y,
          href: m,
          className: c != null && c.call ? c(r === o) : c,
          children: u,
          ref: t,
        });
  }),
  yy = (e) =>
    Array.isArray(e)
      ? e.flatMap((t) => yy(t && t.type === w.Fragment ? t.props.children : t))
      : [e],
  iS = ({ children: e, location: t }) => {
    const n = Pa(),
      [r] = Qc(n);
    for (const i of yy(e)) {
      let s = 0;
      if (
        w.isValidElement(i) &&
        (s = gy(n.parser, i.props.path, t || r, i.props.nest))[0]
      )
        return w.cloneElement(i, { match: s });
    }
    return null;
  };
var Ca = class {
    constructor() {
      (this.listeners = new Set()),
        (this.subscribe = this.subscribe.bind(this));
    }
    subscribe(e) {
      return (
        this.listeners.add(e),
        this.onSubscribe(),
        () => {
          this.listeners.delete(e), this.onUnsubscribe();
        }
      );
    }
    hasListeners() {
      return this.listeners.size > 0;
    }
    onSubscribe() {}
    onUnsubscribe() {}
  },
  Ea = typeof window > "u" || "Deno" in globalThis;
function Pt() {}
function sS(e, t) {
  return typeof e == "function" ? e(t) : e;
}
function oS(e) {
  return typeof e == "number" && e >= 0 && e !== 1 / 0;
}
function aS(e, t) {
  return Math.max(e + (t || 0) - Date.now(), 0);
}
function uh(e, t) {
  return typeof e == "function" ? e(t) : e;
}
function lS(e, t) {
  return typeof e == "function" ? e(t) : e;
}
function ch(e, t) {
  const {
    type: n = "all",
    exact: r,
    fetchStatus: i,
    predicate: s,
    queryKey: o,
    stale: a,
  } = e;
  if (o) {
    if (r) {
      if (t.queryHash !== Gc(o, t.options)) return !1;
    } else if (!ps(t.queryKey, o)) return !1;
  }
  if (n !== "all") {
    const l = t.isActive();
    if ((n === "active" && !l) || (n === "inactive" && l)) return !1;
  }
  return !(
    (typeof a == "boolean" && t.isStale() !== a) ||
    (i && i !== t.state.fetchStatus) ||
    (s && !s(t))
  );
}
function dh(e, t) {
  const { exact: n, status: r, predicate: i, mutationKey: s } = e;
  if (s) {
    if (!t.options.mutationKey) return !1;
    if (n) {
      if (hs(t.options.mutationKey) !== hs(s)) return !1;
    } else if (!ps(t.options.mutationKey, s)) return !1;
  }
  return !((r && t.state.status !== r) || (i && !i(t)));
}
function Gc(e, t) {
  return ((t == null ? void 0 : t.queryKeyHashFn) || hs)(e);
}
function hs(e) {
  return JSON.stringify(e, (t, n) =>
    Tu(n)
      ? Object.keys(n)
          .sort()
          .reduce((r, i) => ((r[i] = n[i]), r), {})
      : n
  );
}
function ps(e, t) {
  return e === t
    ? !0
    : typeof e != typeof t
    ? !1
    : e && t && typeof e == "object" && typeof t == "object"
    ? !Object.keys(t).some((n) => !ps(e[n], t[n]))
    : !1;
}
function vy(e, t) {
  if (e === t) return e;
  const n = fh(e) && fh(t);
  if (n || (Tu(e) && Tu(t))) {
    const r = n ? e : Object.keys(e),
      i = r.length,
      s = n ? t : Object.keys(t),
      o = s.length,
      a = n ? [] : {};
    let l = 0;
    for (let u = 0; u < o; u++) {
      const c = n ? u : s[u];
      ((!n && r.includes(c)) || n) && e[c] === void 0 && t[c] === void 0
        ? ((a[c] = void 0), l++)
        : ((a[c] = vy(e[c], t[c])), a[c] === e[c] && e[c] !== void 0 && l++);
    }
    return i === o && l === i ? e : a;
  }
  return t;
}
function fh(e) {
  return Array.isArray(e) && e.length === Object.keys(e).length;
}
function Tu(e) {
  if (!hh(e)) return !1;
  const t = e.constructor;
  if (t === void 0) return !0;
  const n = t.prototype;
  return !(
    !hh(n) ||
    !n.hasOwnProperty("isPrototypeOf") ||
    Object.getPrototypeOf(e) !== Object.prototype
  );
}
function hh(e) {
  return Object.prototype.toString.call(e) === "[object Object]";
}
function uS(e) {
  return new Promise((t) => {
    setTimeout(t, e);
  });
}
function cS(e, t, n) {
  return typeof n.structuralSharing == "function"
    ? n.structuralSharing(e, t)
    : n.structuralSharing !== !1
    ? vy(e, t)
    : t;
}
function dS(e, t, n = 0) {
  const r = [...e, t];
  return n && r.length > n ? r.slice(1) : r;
}
function fS(e, t, n = 0) {
  const r = [t, ...e];
  return n && r.length > n ? r.slice(0, -1) : r;
}
var qc = Symbol();
function xy(e, t) {
  return !e.queryFn && t != null && t.initialPromise
    ? () => t.initialPromise
    : !e.queryFn || e.queryFn === qc
    ? () => Promise.reject(new Error(`Missing queryFn: '${e.queryHash}'`))
    : e.queryFn;
}
var ir,
  Pn,
  Kr,
  Vp,
  hS =
    ((Vp = class extends Ca {
      constructor() {
        super();
        q(this, ir);
        q(this, Pn);
        q(this, Kr);
        $(this, Kr, (t) => {
          if (!Ea && window.addEventListener) {
            const n = () => t();
            return (
              window.addEventListener("visibilitychange", n, !1),
              () => {
                window.removeEventListener("visibilitychange", n);
              }
            );
          }
        });
      }
      onSubscribe() {
        A(this, Pn) || this.setEventListener(A(this, Kr));
      }
      onUnsubscribe() {
        var t;
        this.hasListeners() ||
          ((t = A(this, Pn)) == null || t.call(this), $(this, Pn, void 0));
      }
      setEventListener(t) {
        var n;
        $(this, Kr, t),
          (n = A(this, Pn)) == null || n.call(this),
          $(
            this,
            Pn,
            t((r) => {
              typeof r == "boolean" ? this.setFocused(r) : this.onFocus();
            })
          );
      }
      setFocused(t) {
        A(this, ir) !== t && ($(this, ir, t), this.onFocus());
      }
      onFocus() {
        const t = this.isFocused();
        this.listeners.forEach((n) => {
          n(t);
        });
      }
      isFocused() {
        var t;
        return typeof A(this, ir) == "boolean"
          ? A(this, ir)
          : ((t = globalThis.document) == null ? void 0 : t.visibilityState) !==
              "hidden";
      }
    }),
    (ir = new WeakMap()),
    (Pn = new WeakMap()),
    (Kr = new WeakMap()),
    Vp),
  wy = new hS(),
  Qr,
  Cn,
  Gr,
  zp,
  pS =
    ((zp = class extends Ca {
      constructor() {
        super();
        q(this, Qr, !0);
        q(this, Cn);
        q(this, Gr);
        $(this, Gr, (t) => {
          if (!Ea && window.addEventListener) {
            const n = () => t(!0),
              r = () => t(!1);
            return (
              window.addEventListener("online", n, !1),
              window.addEventListener("offline", r, !1),
              () => {
                window.removeEventListener("online", n),
                  window.removeEventListener("offline", r);
              }
            );
          }
        });
      }
      onSubscribe() {
        A(this, Cn) || this.setEventListener(A(this, Gr));
      }
      onUnsubscribe() {
        var t;
        this.hasListeners() ||
          ((t = A(this, Cn)) == null || t.call(this), $(this, Cn, void 0));
      }
      setEventListener(t) {
        var n;
        $(this, Gr, t),
          (n = A(this, Cn)) == null || n.call(this),
          $(this, Cn, t(this.setOnline.bind(this)));
      }
      setOnline(t) {
        A(this, Qr) !== t &&
          ($(this, Qr, t),
          this.listeners.forEach((r) => {
            r(t);
          }));
      }
      isOnline() {
        return A(this, Qr);
      }
    }),
    (Qr = new WeakMap()),
    (Cn = new WeakMap()),
    (Gr = new WeakMap()),
    zp),
  Go = new pS();
function mS() {
  let e, t;
  const n = new Promise((i, s) => {
    (e = i), (t = s);
  });
  (n.status = "pending"), n.catch(() => {});
  function r(i) {
    Object.assign(n, i), delete n.resolve, delete n.reject;
  }
  return (
    (n.resolve = (i) => {
      r({ status: "fulfilled", value: i }), e(i);
    }),
    (n.reject = (i) => {
      r({ status: "rejected", reason: i }), t(i);
    }),
    n
  );
}
function gS(e) {
  return Math.min(1e3 * 2 ** e, 3e4);
}
function Sy(e) {
  return (e ?? "online") === "online" ? Go.isOnline() : !0;
}
var Py = class extends Error {
  constructor(e) {
    super("CancelledError"),
      (this.revert = e == null ? void 0 : e.revert),
      (this.silent = e == null ? void 0 : e.silent);
  }
};
function ml(e) {
  return e instanceof Py;
}
function Cy(e) {
  let t = !1,
    n = 0,
    r = !1,
    i;
  const s = mS(),
    o = (m) => {
      var x;
      r || (f(new Py(m)), (x = e.abort) == null || x.call(e));
    },
    a = () => {
      t = !0;
    },
    l = () => {
      t = !1;
    },
    u = () =>
      wy.isFocused() &&
      (e.networkMode === "always" || Go.isOnline()) &&
      e.canRun(),
    c = () => Sy(e.networkMode) && e.canRun(),
    d = (m) => {
      var x;
      r ||
        ((r = !0),
        (x = e.onSuccess) == null || x.call(e, m),
        i == null || i(),
        s.resolve(m));
    },
    f = (m) => {
      var x;
      r ||
        ((r = !0),
        (x = e.onError) == null || x.call(e, m),
        i == null || i(),
        s.reject(m));
    },
    v = () =>
      new Promise((m) => {
        var x;
        (i = (h) => {
          (r || u()) && m(h);
        }),
          (x = e.onPause) == null || x.call(e);
      }).then(() => {
        var m;
        (i = void 0), r || (m = e.onContinue) == null || m.call(e);
      }),
    y = () => {
      if (r) return;
      let m;
      const x = n === 0 ? e.initialPromise : void 0;
      try {
        m = x ?? e.fn();
      } catch (h) {
        m = Promise.reject(h);
      }
      Promise.resolve(m)
        .then(d)
        .catch((h) => {
          var k;
          if (r) return;
          const p = e.retry ?? (Ea ? 0 : 3),
            g = e.retryDelay ?? gS,
            S = typeof g == "function" ? g(n, h) : g,
            C =
              p === !0 ||
              (typeof p == "number" && n < p) ||
              (typeof p == "function" && p(n, h));
          if (t || !C) {
            f(h);
            return;
          }
          n++,
            (k = e.onFail) == null || k.call(e, n, h),
            uS(S)
              .then(() => (u() ? void 0 : v()))
              .then(() => {
                t ? f(h) : y();
              });
        });
    };
  return {
    promise: s,
    cancel: o,
    continue: () => (i == null || i(), s),
    cancelRetry: a,
    continueRetry: l,
    canStart: c,
    start: () => (c() ? y() : v().then(y), s),
  };
}
function yS() {
  let e = [],
    t = 0,
    n = (a) => {
      a();
    },
    r = (a) => {
      a();
    },
    i = (a) => setTimeout(a, 0);
  const s = (a) => {
      t
        ? e.push(a)
        : i(() => {
            n(a);
          });
    },
    o = () => {
      const a = e;
      (e = []),
        a.length &&
          i(() => {
            r(() => {
              a.forEach((l) => {
                n(l);
              });
            });
          });
    };
  return {
    batch: (a) => {
      let l;
      t++;
      try {
        l = a();
      } finally {
        t--, t || o();
      }
      return l;
    },
    batchCalls:
      (a) =>
      (...l) => {
        s(() => {
          a(...l);
        });
      },
    schedule: s,
    setNotifyFunction: (a) => {
      n = a;
    },
    setBatchNotifyFunction: (a) => {
      r = a;
    },
    setScheduler: (a) => {
      i = a;
    },
  };
}
var Ue = yS(),
  sr,
  Bp,
  Ey =
    ((Bp = class {
      constructor() {
        q(this, sr);
      }
      destroy() {
        this.clearGcTimeout();
      }
      scheduleGc() {
        this.clearGcTimeout(),
          oS(this.gcTime) &&
            $(
              this,
              sr,
              setTimeout(() => {
                this.optionalRemove();
              }, this.gcTime)
            );
      }
      updateGcTime(e) {
        this.gcTime = Math.max(
          this.gcTime || 0,
          e ?? (Ea ? 1 / 0 : 5 * 60 * 1e3)
        );
      }
      clearGcTimeout() {
        A(this, sr) && (clearTimeout(A(this, sr)), $(this, sr, void 0));
      }
    }),
    (sr = new WeakMap()),
    Bp),
  qr,
  Xr,
  dt,
  be,
  Cs,
  or,
  Ct,
  Kt,
  Up,
  vS =
    ((Up = class extends Ey {
      constructor(t) {
        super();
        q(this, Ct);
        q(this, qr);
        q(this, Xr);
        q(this, dt);
        q(this, be);
        q(this, Cs);
        q(this, or);
        $(this, or, !1),
          $(this, Cs, t.defaultOptions),
          this.setOptions(t.options),
          (this.observers = []),
          $(this, dt, t.cache),
          (this.queryKey = t.queryKey),
          (this.queryHash = t.queryHash),
          $(this, qr, wS(this.options)),
          (this.state = t.state ?? A(this, qr)),
          this.scheduleGc();
      }
      get meta() {
        return this.options.meta;
      }
      get promise() {
        var t;
        return (t = A(this, be)) == null ? void 0 : t.promise;
      }
      setOptions(t) {
        (this.options = { ...A(this, Cs), ...t }),
          this.updateGcTime(this.options.gcTime);
      }
      optionalRemove() {
        !this.observers.length &&
          this.state.fetchStatus === "idle" &&
          A(this, dt).remove(this);
      }
      setData(t, n) {
        const r = cS(this.state.data, t, this.options);
        return (
          Me(this, Ct, Kt).call(this, {
            data: r,
            type: "success",
            dataUpdatedAt: n == null ? void 0 : n.updatedAt,
            manual: n == null ? void 0 : n.manual,
          }),
          r
        );
      }
      setState(t, n) {
        Me(this, Ct, Kt).call(this, {
          type: "setState",
          state: t,
          setStateOptions: n,
        });
      }
      cancel(t) {
        var r, i;
        const n = (r = A(this, be)) == null ? void 0 : r.promise;
        return (
          (i = A(this, be)) == null || i.cancel(t),
          n ? n.then(Pt).catch(Pt) : Promise.resolve()
        );
      }
      destroy() {
        super.destroy(), this.cancel({ silent: !0 });
      }
      reset() {
        this.destroy(), this.setState(A(this, qr));
      }
      isActive() {
        return this.observers.some((t) => lS(t.options.enabled, this) !== !1);
      }
      isDisabled() {
        return this.getObserversCount() > 0
          ? !this.isActive()
          : this.options.queryFn === qc ||
              this.state.dataUpdateCount + this.state.errorUpdateCount === 0;
      }
      isStale() {
        return this.state.isInvalidated
          ? !0
          : this.getObserversCount() > 0
          ? this.observers.some((t) => t.getCurrentResult().isStale)
          : this.state.data === void 0;
      }
      isStaleByTime(t = 0) {
        return (
          this.state.isInvalidated ||
          this.state.data === void 0 ||
          !aS(this.state.dataUpdatedAt, t)
        );
      }
      onFocus() {
        var n;
        const t = this.observers.find((r) => r.shouldFetchOnWindowFocus());
        t == null || t.refetch({ cancelRefetch: !1 }),
          (n = A(this, be)) == null || n.continue();
      }
      onOnline() {
        var n;
        const t = this.observers.find((r) => r.shouldFetchOnReconnect());
        t == null || t.refetch({ cancelRefetch: !1 }),
          (n = A(this, be)) == null || n.continue();
      }
      addObserver(t) {
        this.observers.includes(t) ||
          (this.observers.push(t),
          this.clearGcTimeout(),
          A(this, dt).notify({
            type: "observerAdded",
            query: this,
            observer: t,
          }));
      }
      removeObserver(t) {
        this.observers.includes(t) &&
          ((this.observers = this.observers.filter((n) => n !== t)),
          this.observers.length ||
            (A(this, be) &&
              (A(this, or)
                ? A(this, be).cancel({ revert: !0 })
                : A(this, be).cancelRetry()),
            this.scheduleGc()),
          A(this, dt).notify({
            type: "observerRemoved",
            query: this,
            observer: t,
          }));
      }
      getObserversCount() {
        return this.observers.length;
      }
      invalidate() {
        this.state.isInvalidated ||
          Me(this, Ct, Kt).call(this, { type: "invalidate" });
      }
      fetch(t, n) {
        var l, u, c;
        if (this.state.fetchStatus !== "idle") {
          if (this.state.data !== void 0 && n != null && n.cancelRefetch)
            this.cancel({ silent: !0 });
          else if (A(this, be))
            return A(this, be).continueRetry(), A(this, be).promise;
        }
        if ((t && this.setOptions(t), !this.options.queryFn)) {
          const d = this.observers.find((f) => f.options.queryFn);
          d && this.setOptions(d.options);
        }
        const r = new AbortController(),
          i = (d) => {
            Object.defineProperty(d, "signal", {
              enumerable: !0,
              get: () => ($(this, or, !0), r.signal),
            });
          },
          s = () => {
            const d = xy(this.options, n),
              f = { queryKey: this.queryKey, meta: this.meta };
            return (
              i(f),
              $(this, or, !1),
              this.options.persister ? this.options.persister(d, f, this) : d(f)
            );
          },
          o = {
            fetchOptions: n,
            options: this.options,
            queryKey: this.queryKey,
            state: this.state,
            fetchFn: s,
          };
        i(o),
          (l = this.options.behavior) == null || l.onFetch(o, this),
          $(this, Xr, this.state),
          (this.state.fetchStatus === "idle" ||
            this.state.fetchMeta !==
              ((u = o.fetchOptions) == null ? void 0 : u.meta)) &&
            Me(this, Ct, Kt).call(this, {
              type: "fetch",
              meta: (c = o.fetchOptions) == null ? void 0 : c.meta,
            });
        const a = (d) => {
          var f, v, y, m;
          (ml(d) && d.silent) ||
            Me(this, Ct, Kt).call(this, { type: "error", error: d }),
            ml(d) ||
              ((v = (f = A(this, dt).config).onError) == null ||
                v.call(f, d, this),
              (m = (y = A(this, dt).config).onSettled) == null ||
                m.call(y, this.state.data, d, this)),
            this.scheduleGc();
        };
        return (
          $(
            this,
            be,
            Cy({
              initialPromise: n == null ? void 0 : n.initialPromise,
              fn: o.fetchFn,
              abort: r.abort.bind(r),
              onSuccess: (d) => {
                var f, v, y, m;
                if (d === void 0) {
                  a(new Error(`${this.queryHash} data is undefined`));
                  return;
                }
                try {
                  this.setData(d);
                } catch (x) {
                  a(x);
                  return;
                }
                (v = (f = A(this, dt).config).onSuccess) == null ||
                  v.call(f, d, this),
                  (m = (y = A(this, dt).config).onSettled) == null ||
                    m.call(y, d, this.state.error, this),
                  this.scheduleGc();
              },
              onError: a,
              onFail: (d, f) => {
                Me(this, Ct, Kt).call(this, {
                  type: "failed",
                  failureCount: d,
                  error: f,
                });
              },
              onPause: () => {
                Me(this, Ct, Kt).call(this, { type: "pause" });
              },
              onContinue: () => {
                Me(this, Ct, Kt).call(this, { type: "continue" });
              },
              retry: o.options.retry,
              retryDelay: o.options.retryDelay,
              networkMode: o.options.networkMode,
              canRun: () => !0,
            })
          ),
          A(this, be).start()
        );
      }
    }),
    (qr = new WeakMap()),
    (Xr = new WeakMap()),
    (dt = new WeakMap()),
    (be = new WeakMap()),
    (Cs = new WeakMap()),
    (or = new WeakMap()),
    (Ct = new WeakSet()),
    (Kt = function (t) {
      const n = (r) => {
        switch (t.type) {
          case "failed":
            return {
              ...r,
              fetchFailureCount: t.failureCount,
              fetchFailureReason: t.error,
            };
          case "pause":
            return { ...r, fetchStatus: "paused" };
          case "continue":
            return { ...r, fetchStatus: "fetching" };
          case "fetch":
            return {
              ...r,
              ...xS(r.data, this.options),
              fetchMeta: t.meta ?? null,
            };
          case "success":
            return {
              ...r,
              data: t.data,
              dataUpdateCount: r.dataUpdateCount + 1,
              dataUpdatedAt: t.dataUpdatedAt ?? Date.now(),
              error: null,
              isInvalidated: !1,
              status: "success",
              ...(!t.manual && {
                fetchStatus: "idle",
                fetchFailureCount: 0,
                fetchFailureReason: null,
              }),
            };
          case "error":
            const i = t.error;
            return ml(i) && i.revert && A(this, Xr)
              ? { ...A(this, Xr), fetchStatus: "idle" }
              : {
                  ...r,
                  error: i,
                  errorUpdateCount: r.errorUpdateCount + 1,
                  errorUpdatedAt: Date.now(),
                  fetchFailureCount: r.fetchFailureCount + 1,
                  fetchFailureReason: i,
                  fetchStatus: "idle",
                  status: "error",
                };
          case "invalidate":
            return { ...r, isInvalidated: !0 };
          case "setState":
            return { ...r, ...t.state };
        }
      };
      (this.state = n(this.state)),
        Ue.batch(() => {
          this.observers.forEach((r) => {
            r.onQueryUpdate();
          }),
            A(this, dt).notify({ query: this, type: "updated", action: t });
        });
    }),
    Up);
function xS(e, t) {
  return {
    fetchFailureCount: 0,
    fetchFailureReason: null,
    fetchStatus: Sy(t.networkMode) ? "fetching" : "paused",
    ...(e === void 0 && { error: null, status: "pending" }),
  };
}
function wS(e) {
  const t =
      typeof e.initialData == "function" ? e.initialData() : e.initialData,
    n = t !== void 0,
    r = n
      ? typeof e.initialDataUpdatedAt == "function"
        ? e.initialDataUpdatedAt()
        : e.initialDataUpdatedAt
      : 0;
  return {
    data: t,
    dataUpdateCount: 0,
    dataUpdatedAt: n ? r ?? Date.now() : 0,
    error: null,
    errorUpdateCount: 0,
    errorUpdatedAt: 0,
    fetchFailureCount: 0,
    fetchFailureReason: null,
    fetchMeta: null,
    isInvalidated: !1,
    status: n ? "success" : "pending",
    fetchStatus: "idle",
  };
}
var Lt,
  $p,
  SS =
    (($p = class extends Ca {
      constructor(t = {}) {
        super();
        q(this, Lt);
        (this.config = t), $(this, Lt, new Map());
      }
      build(t, n, r) {
        const i = n.queryKey,
          s = n.queryHash ?? Gc(i, n);
        let o = this.get(s);
        return (
          o ||
            ((o = new vS({
              cache: this,
              queryKey: i,
              queryHash: s,
              options: t.defaultQueryOptions(n),
              state: r,
              defaultOptions: t.getQueryDefaults(i),
            })),
            this.add(o)),
          o
        );
      }
      add(t) {
        A(this, Lt).has(t.queryHash) ||
          (A(this, Lt).set(t.queryHash, t),
          this.notify({ type: "added", query: t }));
      }
      remove(t) {
        const n = A(this, Lt).get(t.queryHash);
        n &&
          (t.destroy(),
          n === t && A(this, Lt).delete(t.queryHash),
          this.notify({ type: "removed", query: t }));
      }
      clear() {
        Ue.batch(() => {
          this.getAll().forEach((t) => {
            this.remove(t);
          });
        });
      }
      get(t) {
        return A(this, Lt).get(t);
      }
      getAll() {
        return [...A(this, Lt).values()];
      }
      find(t) {
        const n = { exact: !0, ...t };
        return this.getAll().find((r) => ch(n, r));
      }
      findAll(t = {}) {
        const n = this.getAll();
        return Object.keys(t).length > 0 ? n.filter((r) => ch(t, r)) : n;
      }
      notify(t) {
        Ue.batch(() => {
          this.listeners.forEach((n) => {
            n(t);
          });
        });
      }
      onFocus() {
        Ue.batch(() => {
          this.getAll().forEach((t) => {
            t.onFocus();
          });
        });
      }
      onOnline() {
        Ue.batch(() => {
          this.getAll().forEach((t) => {
            t.onOnline();
          });
        });
      }
    }),
    (Lt = new WeakMap()),
    $p),
  Ot,
  ze,
  ar,
  jt,
  gn,
  Wp,
  PS =
    ((Wp = class extends Ey {
      constructor(t) {
        super();
        q(this, jt);
        q(this, Ot);
        q(this, ze);
        q(this, ar);
        (this.mutationId = t.mutationId),
          $(this, ze, t.mutationCache),
          $(this, Ot, []),
          (this.state = t.state || CS()),
          this.setOptions(t.options),
          this.scheduleGc();
      }
      setOptions(t) {
        (this.options = t), this.updateGcTime(this.options.gcTime);
      }
      get meta() {
        return this.options.meta;
      }
      addObserver(t) {
        A(this, Ot).includes(t) ||
          (A(this, Ot).push(t),
          this.clearGcTimeout(),
          A(this, ze).notify({
            type: "observerAdded",
            mutation: this,
            observer: t,
          }));
      }
      removeObserver(t) {
        $(
          this,
          Ot,
          A(this, Ot).filter((n) => n !== t)
        ),
          this.scheduleGc(),
          A(this, ze).notify({
            type: "observerRemoved",
            mutation: this,
            observer: t,
          });
      }
      optionalRemove() {
        A(this, Ot).length ||
          (this.state.status === "pending"
            ? this.scheduleGc()
            : A(this, ze).remove(this));
      }
      continue() {
        var t;
        return (
          ((t = A(this, ar)) == null ? void 0 : t.continue()) ??
          this.execute(this.state.variables)
        );
      }
      async execute(t) {
        var i, s, o, a, l, u, c, d, f, v, y, m, x, h, p, g, S, C, k, T;
        $(
          this,
          ar,
          Cy({
            fn: () =>
              this.options.mutationFn
                ? this.options.mutationFn(t)
                : Promise.reject(new Error("No mutationFn found")),
            onFail: (E, D) => {
              Me(this, jt, gn).call(this, {
                type: "failed",
                failureCount: E,
                error: D,
              });
            },
            onPause: () => {
              Me(this, jt, gn).call(this, { type: "pause" });
            },
            onContinue: () => {
              Me(this, jt, gn).call(this, { type: "continue" });
            },
            retry: this.options.retry ?? 0,
            retryDelay: this.options.retryDelay,
            networkMode: this.options.networkMode,
            canRun: () => A(this, ze).canRun(this),
          })
        );
        const n = this.state.status === "pending",
          r = !A(this, ar).canStart();
        try {
          if (!n) {
            Me(this, jt, gn).call(this, {
              type: "pending",
              variables: t,
              isPaused: r,
            }),
              await ((s = (i = A(this, ze).config).onMutate) == null
                ? void 0
                : s.call(i, t, this));
            const D = await ((a = (o = this.options).onMutate) == null
              ? void 0
              : a.call(o, t));
            D !== this.state.context &&
              Me(this, jt, gn).call(this, {
                type: "pending",
                context: D,
                variables: t,
                isPaused: r,
              });
          }
          const E = await A(this, ar).start();
          return (
            await ((u = (l = A(this, ze).config).onSuccess) == null
              ? void 0
              : u.call(l, E, t, this.state.context, this)),
            await ((d = (c = this.options).onSuccess) == null
              ? void 0
              : d.call(c, E, t, this.state.context)),
            await ((v = (f = A(this, ze).config).onSettled) == null
              ? void 0
              : v.call(
                  f,
                  E,
                  null,
                  this.state.variables,
                  this.state.context,
                  this
                )),
            await ((m = (y = this.options).onSettled) == null
              ? void 0
              : m.call(y, E, null, t, this.state.context)),
            Me(this, jt, gn).call(this, { type: "success", data: E }),
            E
          );
        } catch (E) {
          try {
            throw (
              (await ((h = (x = A(this, ze).config).onError) == null
                ? void 0
                : h.call(x, E, t, this.state.context, this)),
              await ((g = (p = this.options).onError) == null
                ? void 0
                : g.call(p, E, t, this.state.context)),
              await ((C = (S = A(this, ze).config).onSettled) == null
                ? void 0
                : C.call(
                    S,
                    void 0,
                    E,
                    this.state.variables,
                    this.state.context,
                    this
                  )),
              await ((T = (k = this.options).onSettled) == null
                ? void 0
                : T.call(k, void 0, E, t, this.state.context)),
              E)
            );
          } finally {
            Me(this, jt, gn).call(this, { type: "error", error: E });
          }
        } finally {
          A(this, ze).runNext(this);
        }
      }
    }),
    (Ot = new WeakMap()),
    (ze = new WeakMap()),
    (ar = new WeakMap()),
    (jt = new WeakSet()),
    (gn = function (t) {
      const n = (r) => {
        switch (t.type) {
          case "failed":
            return {
              ...r,
              failureCount: t.failureCount,
              failureReason: t.error,
            };
          case "pause":
            return { ...r, isPaused: !0 };
          case "continue":
            return { ...r, isPaused: !1 };
          case "pending":
            return {
              ...r,
              context: t.context,
              data: void 0,
              failureCount: 0,
              failureReason: null,
              error: null,
              isPaused: t.isPaused,
              status: "pending",
              variables: t.variables,
              submittedAt: Date.now(),
            };
          case "success":
            return {
              ...r,
              data: t.data,
              failureCount: 0,
              failureReason: null,
              error: null,
              status: "success",
              isPaused: !1,
            };
          case "error":
            return {
              ...r,
              data: void 0,
              error: t.error,
              failureCount: r.failureCount + 1,
              failureReason: t.error,
              isPaused: !1,
              status: "error",
            };
        }
      };
      (this.state = n(this.state)),
        Ue.batch(() => {
          A(this, Ot).forEach((r) => {
            r.onMutationUpdate(t);
          }),
            A(this, ze).notify({ mutation: this, type: "updated", action: t });
        });
    }),
    Wp);
function CS() {
  return {
    context: void 0,
    data: void 0,
    error: null,
    failureCount: 0,
    failureReason: null,
    isPaused: !1,
    status: "idle",
    variables: void 0,
    submittedAt: 0,
  };
}
var Ze,
  Es,
  Hp,
  ES =
    ((Hp = class extends Ca {
      constructor(t = {}) {
        super();
        q(this, Ze);
        q(this, Es);
        (this.config = t), $(this, Ze, new Map()), $(this, Es, Date.now());
      }
      build(t, n, r) {
        const i = new PS({
          mutationCache: this,
          mutationId: ++Is(this, Es)._,
          options: t.defaultMutationOptions(n),
          state: r,
        });
        return this.add(i), i;
      }
      add(t) {
        const n = eo(t),
          r = A(this, Ze).get(n) ?? [];
        r.push(t),
          A(this, Ze).set(n, r),
          this.notify({ type: "added", mutation: t });
      }
      remove(t) {
        var r;
        const n = eo(t);
        if (A(this, Ze).has(n)) {
          const i =
            (r = A(this, Ze).get(n)) == null
              ? void 0
              : r.filter((s) => s !== t);
          i && (i.length === 0 ? A(this, Ze).delete(n) : A(this, Ze).set(n, i));
        }
        this.notify({ type: "removed", mutation: t });
      }
      canRun(t) {
        var r;
        const n =
          (r = A(this, Ze).get(eo(t))) == null
            ? void 0
            : r.find((i) => i.state.status === "pending");
        return !n || n === t;
      }
      runNext(t) {
        var r;
        const n =
          (r = A(this, Ze).get(eo(t))) == null
            ? void 0
            : r.find((i) => i !== t && i.state.isPaused);
        return (n == null ? void 0 : n.continue()) ?? Promise.resolve();
      }
      clear() {
        Ue.batch(() => {
          this.getAll().forEach((t) => {
            this.remove(t);
          });
        });
      }
      getAll() {
        return [...A(this, Ze).values()].flat();
      }
      find(t) {
        const n = { exact: !0, ...t };
        return this.getAll().find((r) => dh(n, r));
      }
      findAll(t = {}) {
        return this.getAll().filter((n) => dh(t, n));
      }
      notify(t) {
        Ue.batch(() => {
          this.listeners.forEach((n) => {
            n(t);
          });
        });
      }
      resumePausedMutations() {
        const t = this.getAll().filter((n) => n.state.isPaused);
        return Ue.batch(() =>
          Promise.all(t.map((n) => n.continue().catch(Pt)))
        );
      }
    }),
    (Ze = new WeakMap()),
    (Es = new WeakMap()),
    Hp);
function eo(e) {
  var t;
  return (
    ((t = e.options.scope) == null ? void 0 : t.id) ?? String(e.mutationId)
  );
}
function ph(e) {
  return {
    onFetch: (t, n) => {
      var c, d, f, v, y;
      const r = t.options,
        i =
          (f =
            (d = (c = t.fetchOptions) == null ? void 0 : c.meta) == null
              ? void 0
              : d.fetchMore) == null
            ? void 0
            : f.direction,
        s = ((v = t.state.data) == null ? void 0 : v.pages) || [],
        o = ((y = t.state.data) == null ? void 0 : y.pageParams) || [];
      let a = { pages: [], pageParams: [] },
        l = 0;
      const u = async () => {
        let m = !1;
        const x = (g) => {
            Object.defineProperty(g, "signal", {
              enumerable: !0,
              get: () => (
                t.signal.aborted
                  ? (m = !0)
                  : t.signal.addEventListener("abort", () => {
                      m = !0;
                    }),
                t.signal
              ),
            });
          },
          h = xy(t.options, t.fetchOptions),
          p = async (g, S, C) => {
            if (m) return Promise.reject();
            if (S == null && g.pages.length) return Promise.resolve(g);
            const k = {
              queryKey: t.queryKey,
              pageParam: S,
              direction: C ? "backward" : "forward",
              meta: t.options.meta,
            };
            x(k);
            const T = await h(k),
              { maxPages: E } = t.options,
              D = C ? fS : dS;
            return {
              pages: D(g.pages, T, E),
              pageParams: D(g.pageParams, S, E),
            };
          };
        if (i && s.length) {
          const g = i === "backward",
            S = g ? TS : mh,
            C = { pages: s, pageParams: o },
            k = S(r, C);
          a = await p(C, k, g);
        } else {
          const g = e ?? s.length;
          do {
            const S = l === 0 ? o[0] ?? r.initialPageParam : mh(r, a);
            if (l > 0 && S == null) break;
            (a = await p(a, S)), l++;
          } while (l < g);
        }
        return a;
      };
      t.options.persister
        ? (t.fetchFn = () => {
            var m, x;
            return (x = (m = t.options).persister) == null
              ? void 0
              : x.call(
                  m,
                  u,
                  {
                    queryKey: t.queryKey,
                    meta: t.options.meta,
                    signal: t.signal,
                  },
                  n
                );
          })
        : (t.fetchFn = u);
    },
  };
}
function mh(e, { pages: t, pageParams: n }) {
  const r = t.length - 1;
  return t.length > 0 ? e.getNextPageParam(t[r], t, n[r], n) : void 0;
}
function TS(e, { pages: t, pageParams: n }) {
  var r;
  return t.length > 0
    ? (r = e.getPreviousPageParam) == null
      ? void 0
      : r.call(e, t[0], t, n[0], n)
    : void 0;
}
var de,
  En,
  Tn,
  Yr,
  Zr,
  kn,
  Jr,
  ei,
  Kp,
  kS =
    ((Kp = class {
      constructor(e = {}) {
        q(this, de);
        q(this, En);
        q(this, Tn);
        q(this, Yr);
        q(this, Zr);
        q(this, kn);
        q(this, Jr);
        q(this, ei);
        $(this, de, e.queryCache || new SS()),
          $(this, En, e.mutationCache || new ES()),
          $(this, Tn, e.defaultOptions || {}),
          $(this, Yr, new Map()),
          $(this, Zr, new Map()),
          $(this, kn, 0);
      }
      mount() {
        Is(this, kn)._++,
          A(this, kn) === 1 &&
            ($(
              this,
              Jr,
              wy.subscribe(async (e) => {
                e &&
                  (await this.resumePausedMutations(), A(this, de).onFocus());
              })
            ),
            $(
              this,
              ei,
              Go.subscribe(async (e) => {
                e &&
                  (await this.resumePausedMutations(), A(this, de).onOnline());
              })
            ));
      }
      unmount() {
        var e, t;
        Is(this, kn)._--,
          A(this, kn) === 0 &&
            ((e = A(this, Jr)) == null || e.call(this),
            $(this, Jr, void 0),
            (t = A(this, ei)) == null || t.call(this),
            $(this, ei, void 0));
      }
      isFetching(e) {
        return A(this, de).findAll({ ...e, fetchStatus: "fetching" }).length;
      }
      isMutating(e) {
        return A(this, En).findAll({ ...e, status: "pending" }).length;
      }
      getQueryData(e) {
        var n;
        const t = this.defaultQueryOptions({ queryKey: e });
        return (n = A(this, de).get(t.queryHash)) == null
          ? void 0
          : n.state.data;
      }
      ensureQueryData(e) {
        const t = this.getQueryData(e.queryKey);
        if (t === void 0) return this.fetchQuery(e);
        {
          const n = this.defaultQueryOptions(e),
            r = A(this, de).build(this, n);
          return (
            e.revalidateIfStale &&
              r.isStaleByTime(uh(n.staleTime, r)) &&
              this.prefetchQuery(n),
            Promise.resolve(t)
          );
        }
      }
      getQueriesData(e) {
        return A(this, de)
          .findAll(e)
          .map(({ queryKey: t, state: n }) => {
            const r = n.data;
            return [t, r];
          });
      }
      setQueryData(e, t, n) {
        const r = this.defaultQueryOptions({ queryKey: e }),
          i = A(this, de).get(r.queryHash),
          s = i == null ? void 0 : i.state.data,
          o = sS(t, s);
        if (o !== void 0)
          return A(this, de)
            .build(this, r)
            .setData(o, { ...n, manual: !0 });
      }
      setQueriesData(e, t, n) {
        return Ue.batch(() =>
          A(this, de)
            .findAll(e)
            .map(({ queryKey: r }) => [r, this.setQueryData(r, t, n)])
        );
      }
      getQueryState(e) {
        var n;
        const t = this.defaultQueryOptions({ queryKey: e });
        return (n = A(this, de).get(t.queryHash)) == null ? void 0 : n.state;
      }
      removeQueries(e) {
        const t = A(this, de);
        Ue.batch(() => {
          t.findAll(e).forEach((n) => {
            t.remove(n);
          });
        });
      }
      resetQueries(e, t) {
        const n = A(this, de),
          r = { type: "active", ...e };
        return Ue.batch(
          () => (
            n.findAll(e).forEach((i) => {
              i.reset();
            }),
            this.refetchQueries(r, t)
          )
        );
      }
      cancelQueries(e = {}, t = {}) {
        const n = { revert: !0, ...t },
          r = Ue.batch(() =>
            A(this, de)
              .findAll(e)
              .map((i) => i.cancel(n))
          );
        return Promise.all(r).then(Pt).catch(Pt);
      }
      invalidateQueries(e = {}, t = {}) {
        return Ue.batch(() => {
          if (
            (A(this, de)
              .findAll(e)
              .forEach((r) => {
                r.invalidate();
              }),
            e.refetchType === "none")
          )
            return Promise.resolve();
          const n = { ...e, type: e.refetchType ?? e.type ?? "active" };
          return this.refetchQueries(n, t);
        });
      }
      refetchQueries(e = {}, t) {
        const n = {
            ...t,
            cancelRefetch: (t == null ? void 0 : t.cancelRefetch) ?? !0,
          },
          r = Ue.batch(() =>
            A(this, de)
              .findAll(e)
              .filter((i) => !i.isDisabled())
              .map((i) => {
                let s = i.fetch(void 0, n);
                return (
                  n.throwOnError || (s = s.catch(Pt)),
                  i.state.fetchStatus === "paused" ? Promise.resolve() : s
                );
              })
          );
        return Promise.all(r).then(Pt);
      }
      fetchQuery(e) {
        const t = this.defaultQueryOptions(e);
        t.retry === void 0 && (t.retry = !1);
        const n = A(this, de).build(this, t);
        return n.isStaleByTime(uh(t.staleTime, n))
          ? n.fetch(t)
          : Promise.resolve(n.state.data);
      }
      prefetchQuery(e) {
        return this.fetchQuery(e).then(Pt).catch(Pt);
      }
      fetchInfiniteQuery(e) {
        return (e.behavior = ph(e.pages)), this.fetchQuery(e);
      }
      prefetchInfiniteQuery(e) {
        return this.fetchInfiniteQuery(e).then(Pt).catch(Pt);
      }
      ensureInfiniteQueryData(e) {
        return (e.behavior = ph(e.pages)), this.ensureQueryData(e);
      }
      resumePausedMutations() {
        return Go.isOnline()
          ? A(this, En).resumePausedMutations()
          : Promise.resolve();
      }
      getQueryCache() {
        return A(this, de);
      }
      getMutationCache() {
        return A(this, En);
      }
      getDefaultOptions() {
        return A(this, Tn);
      }
      setDefaultOptions(e) {
        $(this, Tn, e);
      }
      setQueryDefaults(e, t) {
        A(this, Yr).set(hs(e), { queryKey: e, defaultOptions: t });
      }
      getQueryDefaults(e) {
        const t = [...A(this, Yr).values()];
        let n = {};
        return (
          t.forEach((r) => {
            ps(e, r.queryKey) && (n = { ...n, ...r.defaultOptions });
          }),
          n
        );
      }
      setMutationDefaults(e, t) {
        A(this, Zr).set(hs(e), { mutationKey: e, defaultOptions: t });
      }
      getMutationDefaults(e) {
        const t = [...A(this, Zr).values()];
        let n = {};
        return (
          t.forEach((r) => {
            ps(e, r.mutationKey) && (n = { ...n, ...r.defaultOptions });
          }),
          n
        );
      }
      defaultQueryOptions(e) {
        if (e._defaulted) return e;
        const t = {
          ...A(this, Tn).queries,
          ...this.getQueryDefaults(e.queryKey),
          ...e,
          _defaulted: !0,
        };
        return (
          t.queryHash || (t.queryHash = Gc(t.queryKey, t)),
          t.refetchOnReconnect === void 0 &&
            (t.refetchOnReconnect = t.networkMode !== "always"),
          t.throwOnError === void 0 && (t.throwOnError = !!t.suspense),
          !t.networkMode && t.persister && (t.networkMode = "offlineFirst"),
          t.enabled !== !0 && t.queryFn === qc && (t.enabled = !1),
          t
        );
      }
      defaultMutationOptions(e) {
        return e != null && e._defaulted
          ? e
          : {
              ...A(this, Tn).mutations,
              ...((e == null ? void 0 : e.mutationKey) &&
                this.getMutationDefaults(e.mutationKey)),
              ...e,
              _defaulted: !0,
            };
      }
      clear() {
        A(this, de).clear(), A(this, En).clear();
      }
    }),
    (de = new WeakMap()),
    (En = new WeakMap()),
    (Tn = new WeakMap()),
    (Yr = new WeakMap()),
    (Zr = new WeakMap()),
    (kn = new WeakMap()),
    (Jr = new WeakMap()),
    (ei = new WeakMap()),
    Kp),
  AS = w.createContext(void 0),
  RS = ({ client: e, children: t }) => (
    w.useEffect(
      () => (
        e.mount(),
        () => {
          e.unmount();
        }
      ),
      [e]
    ),
    P.jsx(AS.Provider, { value: e, children: t })
  );
async function MS(e) {
  if (!e.ok) {
    const t = (await e.text()) || e.statusText;
    throw new Error(`${e.status}: ${t}`);
  }
}
const DS =
    ({ on401: e }) =>
    async ({ queryKey: t }) => {
      const n = await fetch(t[0], { credentials: "include" });
      return e === "returnNull" && n.status === 401
        ? null
        : (await MS(n), await n.json());
    },
  NS = new kS({
    defaultOptions: {
      queries: {
        queryFn: DS({ on401: "throw" }),
        refetchInterval: !1,
        refetchOnWindowFocus: !1,
        staleTime: 1 / 0,
        retry: !1,
      },
      mutations: { retry: !1 },
    },
  }),
  bS = 1,
  LS = 1e6;
let gl = 0;
function OS() {
  return (gl = (gl + 1) % Number.MAX_SAFE_INTEGER), gl.toString();
}
const yl = new Map(),
  gh = (e) => {
    if (yl.has(e)) return;
    const t = setTimeout(() => {
      yl.delete(e), Hi({ type: "REMOVE_TOAST", toastId: e });
    }, LS);
    yl.set(e, t);
  },
  jS = (e, t) => {
    switch (t.type) {
      case "ADD_TOAST":
        return { ...e, toasts: [t.toast, ...e.toasts].slice(0, bS) };
      case "UPDATE_TOAST":
        return {
          ...e,
          toasts: e.toasts.map((n) =>
            n.id === t.toast.id ? { ...n, ...t.toast } : n
          ),
        };
      case "DISMISS_TOAST": {
        const { toastId: n } = t;
        return (
          n
            ? gh(n)
            : e.toasts.forEach((r) => {
                gh(r.id);
              }),
          {
            ...e,
            toasts: e.toasts.map((r) =>
              r.id === n || n === void 0 ? { ...r, open: !1 } : r
            ),
          }
        );
      }
      case "REMOVE_TOAST":
        return t.toastId === void 0
          ? { ...e, toasts: [] }
          : { ...e, toasts: e.toasts.filter((n) => n.id !== t.toastId) };
    }
  },
  xo = [];
let wo = { toasts: [] };
function Hi(e) {
  (wo = jS(wo, e)),
    xo.forEach((t) => {
      t(wo);
    });
}
function IS({ ...e }) {
  const t = OS(),
    n = (i) => Hi({ type: "UPDATE_TOAST", toast: { ...i, id: t } }),
    r = () => Hi({ type: "DISMISS_TOAST", toastId: t });
  return (
    Hi({
      type: "ADD_TOAST",
      toast: {
        ...e,
        id: t,
        open: !0,
        onOpenChange: (i) => {
          i || r();
        },
      },
    }),
    { id: t, dismiss: r, update: n }
  );
}
function FS() {
  const [e, t] = w.useState(wo);
  return (
    w.useEffect(
      () => (
        xo.push(t),
        () => {
          const n = xo.indexOf(t);
          n > -1 && xo.splice(n, 1);
        }
      ),
      [e]
    ),
    {
      ...e,
      toast: IS,
      dismiss: (n) => Hi({ type: "DISMISS_TOAST", toastId: n }),
    }
  );
}
function et(e, t, { checkForDefaultPrevented: n = !0 } = {}) {
  return function (i) {
    if ((e == null || e(i), n === !1 || !i.defaultPrevented))
      return t == null ? void 0 : t(i);
  };
}
function _S(e, t) {
  typeof e == "function" ? e(t) : e != null && (e.current = t);
}
function Ty(...e) {
  return (t) => e.forEach((n) => _S(n, t));
}
function gr(...e) {
  return w.useCallback(Ty(...e), e);
}
function VS(e, t = []) {
  let n = [];
  function r(s, o) {
    const a = w.createContext(o),
      l = n.length;
    n = [...n, o];
    function u(d) {
      const { scope: f, children: v, ...y } = d,
        m = (f == null ? void 0 : f[e][l]) || a,
        x = w.useMemo(() => y, Object.values(y));
      return P.jsx(m.Provider, { value: x, children: v });
    }
    function c(d, f) {
      const v = (f == null ? void 0 : f[e][l]) || a,
        y = w.useContext(v);
      if (y) return y;
      if (o !== void 0) return o;
      throw new Error(`\`${d}\` must be used within \`${s}\``);
    }
    return (u.displayName = s + "Provider"), [u, c];
  }
  const i = () => {
    const s = n.map((o) => w.createContext(o));
    return function (a) {
      const l = (a == null ? void 0 : a[e]) || s;
      return w.useMemo(() => ({ [`__scope${e}`]: { ...a, [e]: l } }), [a, l]);
    };
  };
  return (i.scopeName = e), [r, zS(i, ...t)];
}
function zS(...e) {
  const t = e[0];
  if (e.length === 1) return t;
  const n = () => {
    const r = e.map((i) => ({ useScope: i(), scopeName: i.scopeName }));
    return function (s) {
      const o = r.reduce((a, { useScope: l, scopeName: u }) => {
        const d = l(s)[`__scope${u}`];
        return { ...a, ...d };
      }, {});
      return w.useMemo(() => ({ [`__scope${t.scopeName}`]: o }), [o]);
    };
  };
  return (n.scopeName = t.scopeName), n;
}
var ms = w.forwardRef((e, t) => {
  const { children: n, ...r } = e,
    i = w.Children.toArray(n),
    s = i.find(US);
  if (s) {
    const o = s.props.children,
      a = i.map((l) =>
        l === s
          ? w.Children.count(o) > 1
            ? w.Children.only(null)
            : w.isValidElement(o)
            ? o.props.children
            : null
          : l
      );
    return P.jsx(ku, {
      ...r,
      ref: t,
      children: w.isValidElement(o) ? w.cloneElement(o, void 0, a) : null,
    });
  }
  return P.jsx(ku, { ...r, ref: t, children: n });
});
ms.displayName = "Slot";
var ku = w.forwardRef((e, t) => {
  const { children: n, ...r } = e;
  if (w.isValidElement(n)) {
    const i = WS(n);
    return w.cloneElement(n, { ...$S(r, n.props), ref: t ? Ty(t, i) : i });
  }
  return w.Children.count(n) > 1 ? w.Children.only(null) : null;
});
ku.displayName = "SlotClone";
var BS = ({ children: e }) => P.jsx(P.Fragment, { children: e });
function US(e) {
  return w.isValidElement(e) && e.type === BS;
}
function $S(e, t) {
  const n = { ...t };
  for (const r in t) {
    const i = e[r],
      s = t[r];
    /^on[A-Z]/.test(r)
      ? i && s
        ? (n[r] = (...a) => {
            s(...a), i(...a);
          })
        : i && (n[r] = i)
      : r === "style"
      ? (n[r] = { ...i, ...s })
      : r === "className" && (n[r] = [i, s].filter(Boolean).join(" "));
  }
  return { ...e, ...n };
}
function WS(e) {
  var r, i;
  let t =
      (r = Object.getOwnPropertyDescriptor(e.props, "ref")) == null
        ? void 0
        : r.get,
    n = t && "isReactWarning" in t && t.isReactWarning;
  return n
    ? e.ref
    : ((t =
        (i = Object.getOwnPropertyDescriptor(e, "ref")) == null
          ? void 0
          : i.get),
      (n = t && "isReactWarning" in t && t.isReactWarning),
      n ? e.props.ref : e.props.ref || e.ref);
}
function HS(e) {
  const t = e + "CollectionProvider",
    [n, r] = VS(t),
    [i, s] = n(t, { collectionRef: { current: null }, itemMap: new Map() }),
    o = (v) => {
      const { scope: y, children: m } = v,
        x = mn.useRef(null),
        h = mn.useRef(new Map()).current;
      return P.jsx(i, { scope: y, itemMap: h, collectionRef: x, children: m });
    };
  o.displayName = t;
  const a = e + "CollectionSlot",
    l = mn.forwardRef((v, y) => {
      const { scope: m, children: x } = v,
        h = s(a, m),
        p = gr(y, h.collectionRef);
      return P.jsx(ms, { ref: p, children: x });
    });
  l.displayName = a;
  const u = e + "CollectionItemSlot",
    c = "data-radix-collection-item",
    d = mn.forwardRef((v, y) => {
      const { scope: m, children: x, ...h } = v,
        p = mn.useRef(null),
        g = gr(y, p),
        S = s(u, m);
      return (
        mn.useEffect(
          () => (
            S.itemMap.set(p, { ref: p, ...h }), () => void S.itemMap.delete(p)
          )
        ),
        P.jsx(ms, { [c]: "", ref: g, children: x })
      );
    });
  d.displayName = u;
  function f(v) {
    const y = s(e + "CollectionConsumer", v);
    return mn.useCallback(() => {
      const x = y.collectionRef.current;
      if (!x) return [];
      const h = Array.from(x.querySelectorAll(`[${c}]`));
      return Array.from(y.itemMap.values()).sort(
        (S, C) => h.indexOf(S.ref.current) - h.indexOf(C.ref.current)
      );
    }, [y.collectionRef, y.itemMap]);
  }
  return [{ Provider: o, Slot: l, ItemSlot: d }, f, r];
}
function KS(e, t = []) {
  let n = [];
  function r(s, o) {
    const a = w.createContext(o),
      l = n.length;
    n = [...n, o];
    const u = (d) => {
      var h;
      const { scope: f, children: v, ...y } = d,
        m = ((h = f == null ? void 0 : f[e]) == null ? void 0 : h[l]) || a,
        x = w.useMemo(() => y, Object.values(y));
      return P.jsx(m.Provider, { value: x, children: v });
    };
    u.displayName = s + "Provider";
    function c(d, f) {
      var m;
      const v = ((m = f == null ? void 0 : f[e]) == null ? void 0 : m[l]) || a,
        y = w.useContext(v);
      if (y) return y;
      if (o !== void 0) return o;
      throw new Error(`\`${d}\` must be used within \`${s}\``);
    }
    return [u, c];
  }
  const i = () => {
    const s = n.map((o) => w.createContext(o));
    return function (a) {
      const l = (a == null ? void 0 : a[e]) || s;
      return w.useMemo(() => ({ [`__scope${e}`]: { ...a, [e]: l } }), [a, l]);
    };
  };
  return (i.scopeName = e), [r, QS(i, ...t)];
}
function QS(...e) {
  const t = e[0];
  if (e.length === 1) return t;
  const n = () => {
    const r = e.map((i) => ({ useScope: i(), scopeName: i.scopeName }));
    return function (s) {
      const o = r.reduce((a, { useScope: l, scopeName: u }) => {
        const d = l(s)[`__scope${u}`];
        return { ...a, ...d };
      }, {});
      return w.useMemo(() => ({ [`__scope${t.scopeName}`]: o }), [o]);
    };
  };
  return (n.scopeName = t.scopeName), n;
}
var GS = [
    "a",
    "button",
    "div",
    "form",
    "h2",
    "h3",
    "img",
    "input",
    "label",
    "li",
    "nav",
    "ol",
    "p",
    "span",
    "svg",
    "ul",
  ],
  Bt = GS.reduce((e, t) => {
    const n = w.forwardRef((r, i) => {
      const { asChild: s, ...o } = r,
        a = s ? ms : t;
      return (
        typeof window < "u" && (window[Symbol.for("radix-ui")] = !0),
        P.jsx(a, { ...o, ref: i })
      );
    });
    return (n.displayName = `Primitive.${t}`), { ...e, [t]: n };
  }, {});
function ky(e, t) {
  e && Sa.flushSync(() => e.dispatchEvent(t));
}
function on(e) {
  const t = w.useRef(e);
  return (
    w.useEffect(() => {
      t.current = e;
    }),
    w.useMemo(
      () =>
        (...n) => {
          var r;
          return (r = t.current) == null ? void 0 : r.call(t, ...n);
        },
      []
    )
  );
}
function qS(e, t = globalThis == null ? void 0 : globalThis.document) {
  const n = on(e);
  w.useEffect(() => {
    const r = (i) => {
      i.key === "Escape" && n(i);
    };
    return (
      t.addEventListener("keydown", r, { capture: !0 }),
      () => t.removeEventListener("keydown", r, { capture: !0 })
    );
  }, [n, t]);
}
var XS = "DismissableLayer",
  Au = "dismissableLayer.update",
  YS = "dismissableLayer.pointerDownOutside",
  ZS = "dismissableLayer.focusOutside",
  yh,
  Ay = w.createContext({
    layers: new Set(),
    layersWithOutsidePointerEventsDisabled: new Set(),
    branches: new Set(),
  }),
  Ry = w.forwardRef((e, t) => {
    const {
        disableOutsidePointerEvents: n = !1,
        onEscapeKeyDown: r,
        onPointerDownOutside: i,
        onFocusOutside: s,
        onInteractOutside: o,
        onDismiss: a,
        ...l
      } = e,
      u = w.useContext(Ay),
      [c, d] = w.useState(null),
      f =
        (c == null ? void 0 : c.ownerDocument) ??
        (globalThis == null ? void 0 : globalThis.document),
      [, v] = w.useState({}),
      y = gr(t, (T) => d(T)),
      m = Array.from(u.layers),
      [x] = [...u.layersWithOutsidePointerEventsDisabled].slice(-1),
      h = m.indexOf(x),
      p = c ? m.indexOf(c) : -1,
      g = u.layersWithOutsidePointerEventsDisabled.size > 0,
      S = p >= h,
      C = eP((T) => {
        const E = T.target,
          D = [...u.branches].some((N) => N.contains(E));
        !S ||
          D ||
          (i == null || i(T),
          o == null || o(T),
          T.defaultPrevented || a == null || a());
      }, f),
      k = tP((T) => {
        const E = T.target;
        [...u.branches].some((N) => N.contains(E)) ||
          (s == null || s(T),
          o == null || o(T),
          T.defaultPrevented || a == null || a());
      }, f);
    return (
      qS((T) => {
        p === u.layers.size - 1 &&
          (r == null || r(T),
          !T.defaultPrevented && a && (T.preventDefault(), a()));
      }, f),
      w.useEffect(() => {
        if (c)
          return (
            n &&
              (u.layersWithOutsidePointerEventsDisabled.size === 0 &&
                ((yh = f.body.style.pointerEvents),
                (f.body.style.pointerEvents = "none")),
              u.layersWithOutsidePointerEventsDisabled.add(c)),
            u.layers.add(c),
            vh(),
            () => {
              n &&
                u.layersWithOutsidePointerEventsDisabled.size === 1 &&
                (f.body.style.pointerEvents = yh);
            }
          );
      }, [c, f, n, u]),
      w.useEffect(
        () => () => {
          c &&
            (u.layers.delete(c),
            u.layersWithOutsidePointerEventsDisabled.delete(c),
            vh());
        },
        [c, u]
      ),
      w.useEffect(() => {
        const T = () => v({});
        return (
          document.addEventListener(Au, T),
          () => document.removeEventListener(Au, T)
        );
      }, []),
      P.jsx(Bt.div, {
        ...l,
        ref: y,
        style: {
          pointerEvents: g ? (S ? "auto" : "none") : void 0,
          ...e.style,
        },
        onFocusCapture: et(e.onFocusCapture, k.onFocusCapture),
        onBlurCapture: et(e.onBlurCapture, k.onBlurCapture),
        onPointerDownCapture: et(
          e.onPointerDownCapture,
          C.onPointerDownCapture
        ),
      })
    );
  });
Ry.displayName = XS;
var JS = "DismissableLayerBranch",
  My = w.forwardRef((e, t) => {
    const n = w.useContext(Ay),
      r = w.useRef(null),
      i = gr(t, r);
    return (
      w.useEffect(() => {
        const s = r.current;
        if (s)
          return (
            n.branches.add(s),
            () => {
              n.branches.delete(s);
            }
          );
      }, [n.branches]),
      P.jsx(Bt.div, { ...e, ref: i })
    );
  });
My.displayName = JS;
function eP(e, t = globalThis == null ? void 0 : globalThis.document) {
  const n = on(e),
    r = w.useRef(!1),
    i = w.useRef(() => {});
  return (
    w.useEffect(() => {
      const s = (a) => {
          if (a.target && !r.current) {
            let l = function () {
              Dy(YS, n, u, { discrete: !0 });
            };
            const u = { originalEvent: a };
            a.pointerType === "touch"
              ? (t.removeEventListener("click", i.current),
                (i.current = l),
                t.addEventListener("click", i.current, { once: !0 }))
              : l();
          } else t.removeEventListener("click", i.current);
          r.current = !1;
        },
        o = window.setTimeout(() => {
          t.addEventListener("pointerdown", s);
        }, 0);
      return () => {
        window.clearTimeout(o),
          t.removeEventListener("pointerdown", s),
          t.removeEventListener("click", i.current);
      };
    }, [t, n]),
    { onPointerDownCapture: () => (r.current = !0) }
  );
}
function tP(e, t = globalThis == null ? void 0 : globalThis.document) {
  const n = on(e),
    r = w.useRef(!1);
  return (
    w.useEffect(() => {
      const i = (s) => {
        s.target &&
          !r.current &&
          Dy(ZS, n, { originalEvent: s }, { discrete: !1 });
      };
      return (
        t.addEventListener("focusin", i),
        () => t.removeEventListener("focusin", i)
      );
    }, [t, n]),
    {
      onFocusCapture: () => (r.current = !0),
      onBlurCapture: () => (r.current = !1),
    }
  );
}
function vh() {
  const e = new CustomEvent(Au);
  document.dispatchEvent(e);
}
function Dy(e, t, n, { discrete: r }) {
  const i = n.originalEvent.target,
    s = new CustomEvent(e, { bubbles: !1, cancelable: !0, detail: n });
  t && i.addEventListener(e, t, { once: !0 }),
    r ? ky(i, s) : i.dispatchEvent(s);
}
var nP = Ry,
  rP = My,
  qo = globalThis != null && globalThis.document ? w.useLayoutEffect : () => {},
  iP = "Portal",
  Ny = w.forwardRef((e, t) => {
    var a;
    const { container: n, ...r } = e,
      [i, s] = w.useState(!1);
    qo(() => s(!0), []);
    const o =
      n ||
      (i &&
        ((a = globalThis == null ? void 0 : globalThis.document) == null
          ? void 0
          : a.body));
    return o ? Aw.createPortal(P.jsx(Bt.div, { ...r, ref: t }), o) : null;
  });
Ny.displayName = iP;
function sP(e, t) {
  return w.useReducer((n, r) => t[n][r] ?? n, e);
}
var by = (e) => {
  const { present: t, children: n } = e,
    r = oP(t),
    i =
      typeof n == "function" ? n({ present: r.isPresent }) : w.Children.only(n),
    s = gr(r.ref, aP(i));
  return typeof n == "function" || r.isPresent
    ? w.cloneElement(i, { ref: s })
    : null;
};
by.displayName = "Presence";
function oP(e) {
  const [t, n] = w.useState(),
    r = w.useRef({}),
    i = w.useRef(e),
    s = w.useRef("none"),
    o = e ? "mounted" : "unmounted",
    [a, l] = sP(o, {
      mounted: { UNMOUNT: "unmounted", ANIMATION_OUT: "unmountSuspended" },
      unmountSuspended: { MOUNT: "mounted", ANIMATION_END: "unmounted" },
      unmounted: { MOUNT: "mounted" },
    });
  return (
    w.useEffect(() => {
      const u = to(r.current);
      s.current = a === "mounted" ? u : "none";
    }, [a]),
    qo(() => {
      const u = r.current,
        c = i.current;
      if (c !== e) {
        const f = s.current,
          v = to(u);
        e
          ? l("MOUNT")
          : v === "none" || (u == null ? void 0 : u.display) === "none"
          ? l("UNMOUNT")
          : l(c && f !== v ? "ANIMATION_OUT" : "UNMOUNT"),
          (i.current = e);
      }
    }, [e, l]),
    qo(() => {
      if (t) {
        let u;
        const c = t.ownerDocument.defaultView ?? window,
          d = (v) => {
            const m = to(r.current).includes(v.animationName);
            if (v.target === t && m && (l("ANIMATION_END"), !i.current)) {
              const x = t.style.animationFillMode;
              (t.style.animationFillMode = "forwards"),
                (u = c.setTimeout(() => {
                  t.style.animationFillMode === "forwards" &&
                    (t.style.animationFillMode = x);
                }));
            }
          },
          f = (v) => {
            v.target === t && (s.current = to(r.current));
          };
        return (
          t.addEventListener("animationstart", f),
          t.addEventListener("animationcancel", d),
          t.addEventListener("animationend", d),
          () => {
            c.clearTimeout(u),
              t.removeEventListener("animationstart", f),
              t.removeEventListener("animationcancel", d),
              t.removeEventListener("animationend", d);
          }
        );
      } else l("ANIMATION_END");
    }, [t, l]),
    {
      isPresent: ["mounted", "unmountSuspended"].includes(a),
      ref: w.useCallback((u) => {
        u && (r.current = getComputedStyle(u)), n(u);
      }, []),
    }
  );
}
function to(e) {
  return (e == null ? void 0 : e.animationName) || "none";
}
function aP(e) {
  var r, i;
  let t =
      (r = Object.getOwnPropertyDescriptor(e.props, "ref")) == null
        ? void 0
        : r.get,
    n = t && "isReactWarning" in t && t.isReactWarning;
  return n
    ? e.ref
    : ((t =
        (i = Object.getOwnPropertyDescriptor(e, "ref")) == null
          ? void 0
          : i.get),
      (n = t && "isReactWarning" in t && t.isReactWarning),
      n ? e.props.ref : e.props.ref || e.ref);
}
function lP({ prop: e, defaultProp: t, onChange: n = () => {} }) {
  const [r, i] = uP({ defaultProp: t, onChange: n }),
    s = e !== void 0,
    o = s ? e : r,
    a = on(n),
    l = w.useCallback(
      (u) => {
        if (s) {
          const d = typeof u == "function" ? u(e) : u;
          d !== e && a(d);
        } else i(u);
      },
      [s, e, i, a]
    );
  return [o, l];
}
function uP({ defaultProp: e, onChange: t }) {
  const n = w.useState(e),
    [r] = n,
    i = w.useRef(r),
    s = on(t);
  return (
    w.useEffect(() => {
      i.current !== r && (s(r), (i.current = r));
    }, [r, i, s]),
    n
  );
}
var cP = "VisuallyHidden",
  Xc = w.forwardRef((e, t) =>
    P.jsx(Bt.span, {
      ...e,
      ref: t,
      style: {
        position: "absolute",
        border: 0,
        width: 1,
        height: 1,
        padding: 0,
        margin: -1,
        overflow: "hidden",
        clip: "rect(0, 0, 0, 0)",
        whiteSpace: "nowrap",
        wordWrap: "normal",
        ...e.style,
      },
    })
  );
Xc.displayName = cP;
var Yc = "ToastProvider",
  [Zc, dP, fP] = HS("Toast"),
  [Ly, WR] = KS("Toast", [fP]),
  [hP, Ta] = Ly(Yc),
  Oy = (e) => {
    const {
        __scopeToast: t,
        label: n = "Notification",
        duration: r = 5e3,
        swipeDirection: i = "right",
        swipeThreshold: s = 50,
        children: o,
      } = e,
      [a, l] = w.useState(null),
      [u, c] = w.useState(0),
      d = w.useRef(!1),
      f = w.useRef(!1);
    return (
      n.trim() ||
        console.error(
          `Invalid prop \`label\` supplied to \`${Yc}\`. Expected non-empty \`string\`.`
        ),
      P.jsx(Zc.Provider, {
        scope: t,
        children: P.jsx(hP, {
          scope: t,
          label: n,
          duration: r,
          swipeDirection: i,
          swipeThreshold: s,
          toastCount: u,
          viewport: a,
          onViewportChange: l,
          onToastAdd: w.useCallback(() => c((v) => v + 1), []),
          onToastRemove: w.useCallback(() => c((v) => v - 1), []),
          isFocusedToastEscapeKeyDownRef: d,
          isClosePausedRef: f,
          children: o,
        }),
      })
    );
  };
Oy.displayName = Yc;
var jy = "ToastViewport",
  pP = ["F8"],
  Ru = "toast.viewportPause",
  Mu = "toast.viewportResume",
  Iy = w.forwardRef((e, t) => {
    const {
        __scopeToast: n,
        hotkey: r = pP,
        label: i = "Notifications ({hotkey})",
        ...s
      } = e,
      o = Ta(jy, n),
      a = dP(n),
      l = w.useRef(null),
      u = w.useRef(null),
      c = w.useRef(null),
      d = w.useRef(null),
      f = gr(t, d, o.onViewportChange),
      v = r.join("+").replace(/Key/g, "").replace(/Digit/g, ""),
      y = o.toastCount > 0;
    w.useEffect(() => {
      const x = (h) => {
        var g;
        r.length !== 0 &&
          r.every((S) => h[S] || h.code === S) &&
          ((g = d.current) == null || g.focus());
      };
      return (
        document.addEventListener("keydown", x),
        () => document.removeEventListener("keydown", x)
      );
    }, [r]),
      w.useEffect(() => {
        const x = l.current,
          h = d.current;
        if (y && x && h) {
          const p = () => {
              if (!o.isClosePausedRef.current) {
                const k = new CustomEvent(Ru);
                h.dispatchEvent(k), (o.isClosePausedRef.current = !0);
              }
            },
            g = () => {
              if (o.isClosePausedRef.current) {
                const k = new CustomEvent(Mu);
                h.dispatchEvent(k), (o.isClosePausedRef.current = !1);
              }
            },
            S = (k) => {
              !x.contains(k.relatedTarget) && g();
            },
            C = () => {
              x.contains(document.activeElement) || g();
            };
          return (
            x.addEventListener("focusin", p),
            x.addEventListener("focusout", S),
            x.addEventListener("pointermove", p),
            x.addEventListener("pointerleave", C),
            window.addEventListener("blur", p),
            window.addEventListener("focus", g),
            () => {
              x.removeEventListener("focusin", p),
                x.removeEventListener("focusout", S),
                x.removeEventListener("pointermove", p),
                x.removeEventListener("pointerleave", C),
                window.removeEventListener("blur", p),
                window.removeEventListener("focus", g);
            }
          );
        }
      }, [y, o.isClosePausedRef]);
    const m = w.useCallback(
      ({ tabbingDirection: x }) => {
        const p = a().map((g) => {
          const S = g.ref.current,
            C = [S, ...AP(S)];
          return x === "forwards" ? C : C.reverse();
        });
        return (x === "forwards" ? p.reverse() : p).flat();
      },
      [a]
    );
    return (
      w.useEffect(() => {
        const x = d.current;
        if (x) {
          const h = (p) => {
            var C, k, T;
            const g = p.altKey || p.ctrlKey || p.metaKey;
            if (p.key === "Tab" && !g) {
              const E = document.activeElement,
                D = p.shiftKey;
              if (p.target === x && D) {
                (C = u.current) == null || C.focus();
                return;
              }
              const I = m({ tabbingDirection: D ? "backwards" : "forwards" }),
                Z = I.findIndex((b) => b === E);
              vl(I.slice(Z + 1))
                ? p.preventDefault()
                : D
                ? (k = u.current) == null || k.focus()
                : (T = c.current) == null || T.focus();
            }
          };
          return (
            x.addEventListener("keydown", h),
            () => x.removeEventListener("keydown", h)
          );
        }
      }, [a, m]),
      P.jsxs(rP, {
        ref: l,
        role: "region",
        "aria-label": i.replace("{hotkey}", v),
        tabIndex: -1,
        style: { pointerEvents: y ? void 0 : "none" },
        children: [
          y &&
            P.jsx(Du, {
              ref: u,
              onFocusFromOutsideViewport: () => {
                const x = m({ tabbingDirection: "forwards" });
                vl(x);
              },
            }),
          P.jsx(Zc.Slot, {
            scope: n,
            children: P.jsx(Bt.ol, { tabIndex: -1, ...s, ref: f }),
          }),
          y &&
            P.jsx(Du, {
              ref: c,
              onFocusFromOutsideViewport: () => {
                const x = m({ tabbingDirection: "backwards" });
                vl(x);
              },
            }),
        ],
      })
    );
  });
Iy.displayName = jy;
var Fy = "ToastFocusProxy",
  Du = w.forwardRef((e, t) => {
    const { __scopeToast: n, onFocusFromOutsideViewport: r, ...i } = e,
      s = Ta(Fy, n);
    return P.jsx(Xc, {
      "aria-hidden": !0,
      tabIndex: 0,
      ...i,
      ref: t,
      style: { position: "fixed" },
      onFocus: (o) => {
        var u;
        const a = o.relatedTarget;
        !((u = s.viewport) != null && u.contains(a)) && r();
      },
    });
  });
Du.displayName = Fy;
var ka = "Toast",
  mP = "toast.swipeStart",
  gP = "toast.swipeMove",
  yP = "toast.swipeCancel",
  vP = "toast.swipeEnd",
  _y = w.forwardRef((e, t) => {
    const { forceMount: n, open: r, defaultOpen: i, onOpenChange: s, ...o } = e,
      [a = !0, l] = lP({ prop: r, defaultProp: i, onChange: s });
    return P.jsx(by, {
      present: n || a,
      children: P.jsx(SP, {
        open: a,
        ...o,
        ref: t,
        onClose: () => l(!1),
        onPause: on(e.onPause),
        onResume: on(e.onResume),
        onSwipeStart: et(e.onSwipeStart, (u) => {
          u.currentTarget.setAttribute("data-swipe", "start");
        }),
        onSwipeMove: et(e.onSwipeMove, (u) => {
          const { x: c, y: d } = u.detail.delta;
          u.currentTarget.setAttribute("data-swipe", "move"),
            u.currentTarget.style.setProperty(
              "--radix-toast-swipe-move-x",
              `${c}px`
            ),
            u.currentTarget.style.setProperty(
              "--radix-toast-swipe-move-y",
              `${d}px`
            );
        }),
        onSwipeCancel: et(e.onSwipeCancel, (u) => {
          u.currentTarget.setAttribute("data-swipe", "cancel"),
            u.currentTarget.style.removeProperty("--radix-toast-swipe-move-x"),
            u.currentTarget.style.removeProperty("--radix-toast-swipe-move-y"),
            u.currentTarget.style.removeProperty("--radix-toast-swipe-end-x"),
            u.currentTarget.style.removeProperty("--radix-toast-swipe-end-y");
        }),
        onSwipeEnd: et(e.onSwipeEnd, (u) => {
          const { x: c, y: d } = u.detail.delta;
          u.currentTarget.setAttribute("data-swipe", "end"),
            u.currentTarget.style.removeProperty("--radix-toast-swipe-move-x"),
            u.currentTarget.style.removeProperty("--radix-toast-swipe-move-y"),
            u.currentTarget.style.setProperty(
              "--radix-toast-swipe-end-x",
              `${c}px`
            ),
            u.currentTarget.style.setProperty(
              "--radix-toast-swipe-end-y",
              `${d}px`
            ),
            l(!1);
        }),
      }),
    });
  });
_y.displayName = ka;
var [xP, wP] = Ly(ka, { onClose() {} }),
  SP = w.forwardRef((e, t) => {
    const {
        __scopeToast: n,
        type: r = "foreground",
        duration: i,
        open: s,
        onClose: o,
        onEscapeKeyDown: a,
        onPause: l,
        onResume: u,
        onSwipeStart: c,
        onSwipeMove: d,
        onSwipeCancel: f,
        onSwipeEnd: v,
        ...y
      } = e,
      m = Ta(ka, n),
      [x, h] = w.useState(null),
      p = gr(t, (b) => h(b)),
      g = w.useRef(null),
      S = w.useRef(null),
      C = i || m.duration,
      k = w.useRef(0),
      T = w.useRef(C),
      E = w.useRef(0),
      { onToastAdd: D, onToastRemove: N } = m,
      j = on(() => {
        var H;
        (x == null ? void 0 : x.contains(document.activeElement)) &&
          ((H = m.viewport) == null || H.focus()),
          o();
      }),
      I = w.useCallback(
        (b) => {
          !b ||
            b === 1 / 0 ||
            (window.clearTimeout(E.current),
            (k.current = new Date().getTime()),
            (E.current = window.setTimeout(j, b)));
        },
        [j]
      );
    w.useEffect(() => {
      const b = m.viewport;
      if (b) {
        const H = () => {
            I(T.current), u == null || u();
          },
          G = () => {
            const B = new Date().getTime() - k.current;
            (T.current = T.current - B),
              window.clearTimeout(E.current),
              l == null || l();
          };
        return (
          b.addEventListener(Ru, G),
          b.addEventListener(Mu, H),
          () => {
            b.removeEventListener(Ru, G), b.removeEventListener(Mu, H);
          }
        );
      }
    }, [m.viewport, C, l, u, I]),
      w.useEffect(() => {
        s && !m.isClosePausedRef.current && I(C);
      }, [s, C, m.isClosePausedRef, I]),
      w.useEffect(() => (D(), () => N()), [D, N]);
    const Z = w.useMemo(() => (x ? Hy(x) : null), [x]);
    return m.viewport
      ? P.jsxs(P.Fragment, {
          children: [
            Z &&
              P.jsx(PP, {
                __scopeToast: n,
                role: "status",
                "aria-live": r === "foreground" ? "assertive" : "polite",
                "aria-atomic": !0,
                children: Z,
              }),
            P.jsx(xP, {
              scope: n,
              onClose: j,
              children: Sa.createPortal(
                P.jsx(Zc.ItemSlot, {
                  scope: n,
                  children: P.jsx(nP, {
                    asChild: !0,
                    onEscapeKeyDown: et(a, () => {
                      m.isFocusedToastEscapeKeyDownRef.current || j(),
                        (m.isFocusedToastEscapeKeyDownRef.current = !1);
                    }),
                    children: P.jsx(Bt.li, {
                      role: "status",
                      "aria-live": "off",
                      "aria-atomic": !0,
                      tabIndex: 0,
                      "data-state": s ? "open" : "closed",
                      "data-swipe-direction": m.swipeDirection,
                      ...y,
                      ref: p,
                      style: {
                        userSelect: "none",
                        touchAction: "none",
                        ...e.style,
                      },
                      onKeyDown: et(e.onKeyDown, (b) => {
                        b.key === "Escape" &&
                          (a == null || a(b.nativeEvent),
                          b.nativeEvent.defaultPrevented ||
                            ((m.isFocusedToastEscapeKeyDownRef.current = !0),
                            j()));
                      }),
                      onPointerDown: et(e.onPointerDown, (b) => {
                        b.button === 0 &&
                          (g.current = { x: b.clientX, y: b.clientY });
                      }),
                      onPointerMove: et(e.onPointerMove, (b) => {
                        if (!g.current) return;
                        const H = b.clientX - g.current.x,
                          G = b.clientY - g.current.y,
                          B = !!S.current,
                          R = ["left", "right"].includes(m.swipeDirection),
                          L = ["left", "up"].includes(m.swipeDirection)
                            ? Math.min
                            : Math.max,
                          F = R ? L(0, H) : 0,
                          z = R ? 0 : L(0, G),
                          Q = b.pointerType === "touch" ? 10 : 2,
                          xe = { x: F, y: z },
                          ge = { originalEvent: b, delta: xe };
                        B
                          ? ((S.current = xe), no(gP, d, ge, { discrete: !1 }))
                          : xh(xe, m.swipeDirection, Q)
                          ? ((S.current = xe),
                            no(mP, c, ge, { discrete: !1 }),
                            b.target.setPointerCapture(b.pointerId))
                          : (Math.abs(H) > Q || Math.abs(G) > Q) &&
                            (g.current = null);
                      }),
                      onPointerUp: et(e.onPointerUp, (b) => {
                        const H = S.current,
                          G = b.target;
                        if (
                          (G.hasPointerCapture(b.pointerId) &&
                            G.releasePointerCapture(b.pointerId),
                          (S.current = null),
                          (g.current = null),
                          H)
                        ) {
                          const B = b.currentTarget,
                            R = { originalEvent: b, delta: H };
                          xh(H, m.swipeDirection, m.swipeThreshold)
                            ? no(vP, v, R, { discrete: !0 })
                            : no(yP, f, R, { discrete: !0 }),
                            B.addEventListener(
                              "click",
                              (L) => L.preventDefault(),
                              { once: !0 }
                            );
                        }
                      }),
                    }),
                  }),
                }),
                m.viewport
              ),
            }),
          ],
        })
      : null;
  }),
  PP = (e) => {
    const { __scopeToast: t, children: n, ...r } = e,
      i = Ta(ka, t),
      [s, o] = w.useState(!1),
      [a, l] = w.useState(!1);
    return (
      TP(() => o(!0)),
      w.useEffect(() => {
        const u = window.setTimeout(() => l(!0), 1e3);
        return () => window.clearTimeout(u);
      }, []),
      a
        ? null
        : P.jsx(Ny, {
            asChild: !0,
            children: P.jsx(Xc, {
              ...r,
              children:
                s && P.jsxs(P.Fragment, { children: [i.label, " ", n] }),
            }),
          })
    );
  },
  CP = "ToastTitle",
  Vy = w.forwardRef((e, t) => {
    const { __scopeToast: n, ...r } = e;
    return P.jsx(Bt.div, { ...r, ref: t });
  });
Vy.displayName = CP;
var EP = "ToastDescription",
  zy = w.forwardRef((e, t) => {
    const { __scopeToast: n, ...r } = e;
    return P.jsx(Bt.div, { ...r, ref: t });
  });
zy.displayName = EP;
var By = "ToastAction",
  Uy = w.forwardRef((e, t) => {
    const { altText: n, ...r } = e;
    return n.trim()
      ? P.jsx(Wy, {
          altText: n,
          asChild: !0,
          children: P.jsx(Jc, { ...r, ref: t }),
        })
      : (console.error(
          `Invalid prop \`altText\` supplied to \`${By}\`. Expected non-empty \`string\`.`
        ),
        null);
  });
Uy.displayName = By;
var $y = "ToastClose",
  Jc = w.forwardRef((e, t) => {
    const { __scopeToast: n, ...r } = e,
      i = wP($y, n);
    return P.jsx(Wy, {
      asChild: !0,
      children: P.jsx(Bt.button, {
        type: "button",
        ...r,
        ref: t,
        onClick: et(e.onClick, i.onClose),
      }),
    });
  });
Jc.displayName = $y;
var Wy = w.forwardRef((e, t) => {
  const { __scopeToast: n, altText: r, ...i } = e;
  return P.jsx(Bt.div, {
    "data-radix-toast-announce-exclude": "",
    "data-radix-toast-announce-alt": r || void 0,
    ...i,
    ref: t,
  });
});
function Hy(e) {
  const t = [];
  return (
    Array.from(e.childNodes).forEach((r) => {
      if (
        (r.nodeType === r.TEXT_NODE && r.textContent && t.push(r.textContent),
        kP(r))
      ) {
        const i = r.ariaHidden || r.hidden || r.style.display === "none",
          s = r.dataset.radixToastAnnounceExclude === "";
        if (!i)
          if (s) {
            const o = r.dataset.radixToastAnnounceAlt;
            o && t.push(o);
          } else t.push(...Hy(r));
      }
    }),
    t
  );
}
function no(e, t, n, { discrete: r }) {
  const i = n.originalEvent.currentTarget,
    s = new CustomEvent(e, { bubbles: !0, cancelable: !0, detail: n });
  t && i.addEventListener(e, t, { once: !0 }),
    r ? ky(i, s) : i.dispatchEvent(s);
}
var xh = (e, t, n = 0) => {
  const r = Math.abs(e.x),
    i = Math.abs(e.y),
    s = r > i;
  return t === "left" || t === "right" ? s && r > n : !s && i > n;
};
function TP(e = () => {}) {
  const t = on(e);
  qo(() => {
    let n = 0,
      r = 0;
    return (
      (n = window.requestAnimationFrame(
        () => (r = window.requestAnimationFrame(t))
      )),
      () => {
        window.cancelAnimationFrame(n), window.cancelAnimationFrame(r);
      }
    );
  }, [t]);
}
function kP(e) {
  return e.nodeType === e.ELEMENT_NODE;
}
function AP(e) {
  const t = [],
    n = document.createTreeWalker(e, NodeFilter.SHOW_ELEMENT, {
      acceptNode: (r) => {
        const i = r.tagName === "INPUT" && r.type === "hidden";
        return r.disabled || r.hidden || i
          ? NodeFilter.FILTER_SKIP
          : r.tabIndex >= 0
          ? NodeFilter.FILTER_ACCEPT
          : NodeFilter.FILTER_SKIP;
      },
    });
  for (; n.nextNode(); ) t.push(n.currentNode);
  return t;
}
function vl(e) {
  const t = document.activeElement;
  return e.some((n) =>
    n === t ? !0 : (n.focus(), document.activeElement !== t)
  );
}
var RP = Oy,
  Ky = Iy,
  Qy = _y,
  Gy = Vy,
  qy = zy,
  Xy = Uy,
  Yy = Jc;
function Zy(e) {
  var t,
    n,
    r = "";
  if (typeof e == "string" || typeof e == "number") r += e;
  else if (typeof e == "object")
    if (Array.isArray(e))
      for (t = 0; t < e.length; t++)
        e[t] && (n = Zy(e[t])) && (r && (r += " "), (r += n));
    else for (t in e) e[t] && (r && (r += " "), (r += t));
  return r;
}
function MP() {
  for (var e, t, n = 0, r = ""; n < arguments.length; )
    (e = arguments[n++]) && (t = Zy(e)) && (r && (r += " "), (r += t));
  return r;
}
const wh = (e) => (typeof e == "boolean" ? "".concat(e) : e === 0 ? "0" : e),
  Sh = MP,
  Jy = (e, t) => (n) => {
    var r;
    if ((t == null ? void 0 : t.variants) == null)
      return Sh(
        e,
        n == null ? void 0 : n.class,
        n == null ? void 0 : n.className
      );
    const { variants: i, defaultVariants: s } = t,
      o = Object.keys(i).map((u) => {
        const c = n == null ? void 0 : n[u],
          d = s == null ? void 0 : s[u];
        if (c === null) return null;
        const f = wh(c) || wh(d);
        return i[u][f];
      }),
      a =
        n &&
        Object.entries(n).reduce((u, c) => {
          let [d, f] = c;
          return f === void 0 || (u[d] = f), u;
        }, {}),
      l =
        t == null || (r = t.compoundVariants) === null || r === void 0
          ? void 0
          : r.reduce((u, c) => {
              let { class: d, className: f, ...v } = c;
              return Object.entries(v).every((y) => {
                let [m, x] = y;
                return Array.isArray(x)
                  ? x.includes({ ...s, ...a }[m])
                  : { ...s, ...a }[m] === x;
              })
                ? [...u, d, f]
                : u;
            }, []);
    return Sh(
      e,
      o,
      l,
      n == null ? void 0 : n.class,
      n == null ? void 0 : n.className
    );
  };
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const DP = (e) => e.replace(/([a-z0-9])([A-Z])/g, "$1-$2").toLowerCase(),
  ev = (...e) => e.filter((t, n, r) => !!t && r.indexOf(t) === n).join(" ");
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ var NP = {
  xmlns: "http://www.w3.org/2000/svg",
  width: 24,
  height: 24,
  viewBox: "0 0 24 24",
  fill: "none",
  stroke: "currentColor",
  strokeWidth: 2,
  strokeLinecap: "round",
  strokeLinejoin: "round",
};
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const bP = w.forwardRef(
  (
    {
      color: e = "currentColor",
      size: t = 24,
      strokeWidth: n = 2,
      absoluteStrokeWidth: r,
      className: i = "",
      children: s,
      iconNode: o,
      ...a
    },
    l
  ) =>
    w.createElement(
      "svg",
      {
        ref: l,
        ...NP,
        width: t,
        height: t,
        stroke: e,
        strokeWidth: r ? (Number(n) * 24) / Number(t) : n,
        className: ev("lucide", i),
        ...a,
      },
      [
        ...o.map(([u, c]) => w.createElement(u, c)),
        ...(Array.isArray(s) ? s : [s]),
      ]
    )
);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const vt = (e, t) => {
  const n = w.forwardRef(({ className: r, ...i }, s) =>
    w.createElement(bP, {
      ref: s,
      iconNode: t,
      className: ev(`lucide-${DP(e)}`, r),
      ...i,
    })
  );
  return (n.displayName = `${e}`), n;
};
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const tv = vt("Award", [
  [
    "path",
    {
      d: "m15.477 12.89 1.515 8.526a.5.5 0 0 1-.81.47l-3.58-2.687a1 1 0 0 0-1.197 0l-3.586 2.686a.5.5 0 0 1-.81-.469l1.514-8.526",
      key: "1yiouv",
    },
  ],
  ["circle", { cx: "12", cy: "8", r: "6", key: "1vp47v" }],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const LP = vt("ChevronLeft", [
  ["path", { d: "m15 18-6-6 6-6", key: "1wnfg3" }],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const OP = vt("ChevronRight", [
  ["path", { d: "m9 18 6-6-6-6", key: "mthhwq" }],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const jP = vt("CircleAlert", [
  ["circle", { cx: "12", cy: "12", r: "10", key: "1mglay" }],
  ["line", { x1: "12", x2: "12", y1: "8", y2: "12", key: "1pkeuh" }],
  ["line", { x1: "12", x2: "12.01", y1: "16", y2: "16", key: "4dfq90" }],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const IP = vt("Clock", [
  ["circle", { cx: "12", cy: "12", r: "10", key: "1mglay" }],
  ["polyline", { points: "12 6 12 12 16 14", key: "68esgv" }],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const FP = vt("Mail", [
  [
    "rect",
    { width: "20", height: "16", x: "2", y: "4", rx: "2", key: "18n3k1" },
  ],
  ["path", { d: "m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7", key: "1ocrg3" }],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const _P = vt("MapPin", [
  [
    "path",
    {
      d: "M20 10c0 4.993-5.539 10.193-7.399 11.799a1 1 0 0 1-1.202 0C9.539 20.193 4 14.993 4 10a8 8 0 0 1 16 0",
      key: "1r0f0z",
    },
  ],
  ["circle", { cx: "12", cy: "10", r: "3", key: "ilqhr7" }],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const VP = vt("Menu", [
  ["line", { x1: "4", x2: "20", y1: "12", y2: "12", key: "1e0a9i" }],
  ["line", { x1: "4", x2: "20", y1: "6", y2: "6", key: "1owob3" }],
  ["line", { x1: "4", x2: "20", y1: "18", y2: "18", key: "yk5zj1" }],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const zP = vt("Phone", [
  [
    "path",
    {
      d: "M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z",
      key: "foiqr5",
    },
  ],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const BP = vt("Shield", [
  [
    "path",
    {
      d: "M20 13c0 5-3.5 7.5-7.66 8.95a1 1 0 0 1-.67-.01C7.5 20.5 4 18 4 13V6a1 1 0 0 1 1-1c2 0 4.5-1.2 6.24-2.72a1.17 1.17 0 0 1 1.52 0C14.51 3.81 17 5 19 5a1 1 0 0 1 1 1z",
      key: "oel41y",
    },
  ],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const UP = vt("Wrench", [
  [
    "path",
    {
      d: "M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z",
      key: "cbrjhi",
    },
  ],
]);
/**
 * @license lucide-react v0.453.0 - ISC
 *
 * This source code is licensed under the ISC license.
 * See the LICENSE file in the root directory of this source tree.
 */ const nv = vt("X", [
  ["path", { d: "M18 6 6 18", key: "1bl5f8" }],
  ["path", { d: "m6 6 12 12", key: "d8bk6v" }],
]);
function rv(e) {
  var t,
    n,
    r = "";
  if (typeof e == "string" || typeof e == "number") r += e;
  else if (typeof e == "object")
    if (Array.isArray(e)) {
      var i = e.length;
      for (t = 0; t < i; t++)
        e[t] && (n = rv(e[t])) && (r && (r += " "), (r += n));
    } else for (n in e) e[n] && (r && (r += " "), (r += n));
  return r;
}
function $P() {
  for (var e, t, n = 0, r = "", i = arguments.length; n < i; n++)
    (e = arguments[n]) && (t = rv(e)) && (r && (r += " "), (r += t));
  return r;
}
const ed = "-",
  WP = (e) => {
    const t = KP(e),
      { conflictingClassGroups: n, conflictingClassGroupModifiers: r } = e;
    return {
      getClassGroupId: (o) => {
        const a = o.split(ed);
        return a[0] === "" && a.length !== 1 && a.shift(), iv(a, t) || HP(o);
      },
      getConflictingClassGroupIds: (o, a) => {
        const l = n[o] || [];
        return a && r[o] ? [...l, ...r[o]] : l;
      },
    };
  },
  iv = (e, t) => {
    var o;
    if (e.length === 0) return t.classGroupId;
    const n = e[0],
      r = t.nextPart.get(n),
      i = r ? iv(e.slice(1), r) : void 0;
    if (i) return i;
    if (t.validators.length === 0) return;
    const s = e.join(ed);
    return (o = t.validators.find(({ validator: a }) => a(s))) == null
      ? void 0
      : o.classGroupId;
  },
  Ph = /^\[(.+)\]$/,
  HP = (e) => {
    if (Ph.test(e)) {
      const t = Ph.exec(e)[1],
        n = t == null ? void 0 : t.substring(0, t.indexOf(":"));
      if (n) return "arbitrary.." + n;
    }
  },
  KP = (e) => {
    const { theme: t, prefix: n } = e,
      r = { nextPart: new Map(), validators: [] };
    return (
      GP(Object.entries(e.classGroups), n).forEach(([s, o]) => {
        Nu(o, r, s, t);
      }),
      r
    );
  },
  Nu = (e, t, n, r) => {
    e.forEach((i) => {
      if (typeof i == "string") {
        const s = i === "" ? t : Ch(t, i);
        s.classGroupId = n;
        return;
      }
      if (typeof i == "function") {
        if (QP(i)) {
          Nu(i(r), t, n, r);
          return;
        }
        t.validators.push({ validator: i, classGroupId: n });
        return;
      }
      Object.entries(i).forEach(([s, o]) => {
        Nu(o, Ch(t, s), n, r);
      });
    });
  },
  Ch = (e, t) => {
    let n = e;
    return (
      t.split(ed).forEach((r) => {
        n.nextPart.has(r) ||
          n.nextPart.set(r, { nextPart: new Map(), validators: [] }),
          (n = n.nextPart.get(r));
      }),
      n
    );
  },
  QP = (e) => e.isThemeGetter,
  GP = (e, t) =>
    t
      ? e.map(([n, r]) => {
          const i = r.map((s) =>
            typeof s == "string"
              ? t + s
              : typeof s == "object"
              ? Object.fromEntries(
                  Object.entries(s).map(([o, a]) => [t + o, a])
                )
              : s
          );
          return [n, i];
        })
      : e,
  qP = (e) => {
    if (e < 1) return { get: () => {}, set: () => {} };
    let t = 0,
      n = new Map(),
      r = new Map();
    const i = (s, o) => {
      n.set(s, o), t++, t > e && ((t = 0), (r = n), (n = new Map()));
    };
    return {
      get(s) {
        let o = n.get(s);
        if (o !== void 0) return o;
        if ((o = r.get(s)) !== void 0) return i(s, o), o;
      },
      set(s, o) {
        n.has(s) ? n.set(s, o) : i(s, o);
      },
    };
  },
  sv = "!",
  XP = (e) => {
    const { separator: t, experimentalParseClassName: n } = e,
      r = t.length === 1,
      i = t[0],
      s = t.length,
      o = (a) => {
        const l = [];
        let u = 0,
          c = 0,
          d;
        for (let x = 0; x < a.length; x++) {
          let h = a[x];
          if (u === 0) {
            if (h === i && (r || a.slice(x, x + s) === t)) {
              l.push(a.slice(c, x)), (c = x + s);
              continue;
            }
            if (h === "/") {
              d = x;
              continue;
            }
          }
          h === "[" ? u++ : h === "]" && u--;
        }
        const f = l.length === 0 ? a : a.substring(c),
          v = f.startsWith(sv),
          y = v ? f.substring(1) : f,
          m = d && d > c ? d - c : void 0;
        return {
          modifiers: l,
          hasImportantModifier: v,
          baseClassName: y,
          maybePostfixModifierPosition: m,
        };
      };
    return n ? (a) => n({ className: a, parseClassName: o }) : o;
  },
  YP = (e) => {
    if (e.length <= 1) return e;
    const t = [];
    let n = [];
    return (
      e.forEach((r) => {
        r[0] === "[" ? (t.push(...n.sort(), r), (n = [])) : n.push(r);
      }),
      t.push(...n.sort()),
      t
    );
  },
  ZP = (e) => ({ cache: qP(e.cacheSize), parseClassName: XP(e), ...WP(e) }),
  JP = /\s+/,
  eC = (e, t) => {
    const {
        parseClassName: n,
        getClassGroupId: r,
        getConflictingClassGroupIds: i,
      } = t,
      s = [],
      o = e.trim().split(JP);
    let a = "";
    for (let l = o.length - 1; l >= 0; l -= 1) {
      const u = o[l],
        {
          modifiers: c,
          hasImportantModifier: d,
          baseClassName: f,
          maybePostfixModifierPosition: v,
        } = n(u);
      let y = !!v,
        m = r(y ? f.substring(0, v) : f);
      if (!m) {
        if (!y) {
          a = u + (a.length > 0 ? " " + a : a);
          continue;
        }
        if (((m = r(f)), !m)) {
          a = u + (a.length > 0 ? " " + a : a);
          continue;
        }
        y = !1;
      }
      const x = YP(c).join(":"),
        h = d ? x + sv : x,
        p = h + m;
      if (s.includes(p)) continue;
      s.push(p);
      const g = i(m, y);
      for (let S = 0; S < g.length; ++S) {
        const C = g[S];
        s.push(h + C);
      }
      a = u + (a.length > 0 ? " " + a : a);
    }
    return a;
  };
function tC() {
  let e = 0,
    t,
    n,
    r = "";
  for (; e < arguments.length; )
    (t = arguments[e++]) && (n = ov(t)) && (r && (r += " "), (r += n));
  return r;
}
const ov = (e) => {
  if (typeof e == "string") return e;
  let t,
    n = "";
  for (let r = 0; r < e.length; r++)
    e[r] && (t = ov(e[r])) && (n && (n += " "), (n += t));
  return n;
};
function nC(e, ...t) {
  let n,
    r,
    i,
    s = o;
  function o(l) {
    const u = t.reduce((c, d) => d(c), e());
    return (n = ZP(u)), (r = n.cache.get), (i = n.cache.set), (s = a), a(l);
  }
  function a(l) {
    const u = r(l);
    if (u) return u;
    const c = eC(l, n);
    return i(l, c), c;
  }
  return function () {
    return s(tC.apply(null, arguments));
  };
}
const te = (e) => {
    const t = (n) => n[e] || [];
    return (t.isThemeGetter = !0), t;
  },
  av = /^\[(?:([a-z-]+):)?(.+)\]$/i,
  rC = /^\d+\/\d+$/,
  iC = new Set(["px", "full", "screen"]),
  sC = /^(\d+(\.\d+)?)?(xs|sm|md|lg|xl)$/,
  oC =
    /\d+(%|px|r?em|[sdl]?v([hwib]|min|max)|pt|pc|in|cm|mm|cap|ch|ex|r?lh|cq(w|h|i|b|min|max))|\b(calc|min|max|clamp)\(.+\)|^0$/,
  aC = /^(rgba?|hsla?|hwb|(ok)?(lab|lch))\(.+\)$/,
  lC = /^(inset_)?-?((\d+)?\.?(\d+)[a-z]+|0)_-?((\d+)?\.?(\d+)[a-z]+|0)/,
  uC =
    /^(url|image|image-set|cross-fade|element|(repeating-)?(linear|radial|conic)-gradient)\(.+\)$/,
  Ht = (e) => Hr(e) || iC.has(e) || rC.test(e),
  hn = (e) => mi(e, "length", yC),
  Hr = (e) => !!e && !Number.isNaN(Number(e)),
  xl = (e) => mi(e, "number", Hr),
  ki = (e) => !!e && Number.isInteger(Number(e)),
  cC = (e) => e.endsWith("%") && Hr(e.slice(0, -1)),
  U = (e) => av.test(e),
  pn = (e) => sC.test(e),
  dC = new Set(["length", "size", "percentage"]),
  fC = (e) => mi(e, dC, lv),
  hC = (e) => mi(e, "position", lv),
  pC = new Set(["image", "url"]),
  mC = (e) => mi(e, pC, xC),
  gC = (e) => mi(e, "", vC),
  Ai = () => !0,
  mi = (e, t, n) => {
    const r = av.exec(e);
    return r
      ? r[1]
        ? typeof t == "string"
          ? r[1] === t
          : t.has(r[1])
        : n(r[2])
      : !1;
  },
  yC = (e) => oC.test(e) && !aC.test(e),
  lv = () => !1,
  vC = (e) => lC.test(e),
  xC = (e) => uC.test(e),
  wC = () => {
    const e = te("colors"),
      t = te("spacing"),
      n = te("blur"),
      r = te("brightness"),
      i = te("borderColor"),
      s = te("borderRadius"),
      o = te("borderSpacing"),
      a = te("borderWidth"),
      l = te("contrast"),
      u = te("grayscale"),
      c = te("hueRotate"),
      d = te("invert"),
      f = te("gap"),
      v = te("gradientColorStops"),
      y = te("gradientColorStopPositions"),
      m = te("inset"),
      x = te("margin"),
      h = te("opacity"),
      p = te("padding"),
      g = te("saturate"),
      S = te("scale"),
      C = te("sepia"),
      k = te("skew"),
      T = te("space"),
      E = te("translate"),
      D = () => ["auto", "contain", "none"],
      N = () => ["auto", "hidden", "clip", "visible", "scroll"],
      j = () => ["auto", U, t],
      I = () => [U, t],
      Z = () => ["", Ht, hn],
      b = () => ["auto", Hr, U],
      H = () => [
        "bottom",
        "center",
        "left",
        "left-bottom",
        "left-top",
        "right",
        "right-bottom",
        "right-top",
        "top",
      ],
      G = () => ["solid", "dashed", "dotted", "double", "none"],
      B = () => [
        "normal",
        "multiply",
        "screen",
        "overlay",
        "darken",
        "lighten",
        "color-dodge",
        "color-burn",
        "hard-light",
        "soft-light",
        "difference",
        "exclusion",
        "hue",
        "saturation",
        "color",
        "luminosity",
      ],
      R = () => [
        "start",
        "end",
        "center",
        "between",
        "around",
        "evenly",
        "stretch",
      ],
      L = () => ["", "0", U],
      F = () => [
        "auto",
        "avoid",
        "all",
        "avoid-page",
        "page",
        "left",
        "right",
        "column",
      ],
      z = () => [Hr, U];
    return {
      cacheSize: 500,
      separator: ":",
      theme: {
        colors: [Ai],
        spacing: [Ht, hn],
        blur: ["none", "", pn, U],
        brightness: z(),
        borderColor: [e],
        borderRadius: ["none", "", "full", pn, U],
        borderSpacing: I(),
        borderWidth: Z(),
        contrast: z(),
        grayscale: L(),
        hueRotate: z(),
        invert: L(),
        gap: I(),
        gradientColorStops: [e],
        gradientColorStopPositions: [cC, hn],
        inset: j(),
        margin: j(),
        opacity: z(),
        padding: I(),
        saturate: z(),
        scale: z(),
        sepia: L(),
        skew: z(),
        space: I(),
        translate: I(),
      },
      classGroups: {
        aspect: [{ aspect: ["auto", "square", "video", U] }],
        container: ["container"],
        columns: [{ columns: [pn] }],
        "break-after": [{ "break-after": F() }],
        "break-before": [{ "break-before": F() }],
        "break-inside": [
          { "break-inside": ["auto", "avoid", "avoid-page", "avoid-column"] },
        ],
        "box-decoration": [{ "box-decoration": ["slice", "clone"] }],
        box: [{ box: ["border", "content"] }],
        display: [
          "block",
          "inline-block",
          "inline",
          "flex",
          "inline-flex",
          "table",
          "inline-table",
          "table-caption",
          "table-cell",
          "table-column",
          "table-column-group",
          "table-footer-group",
          "table-header-group",
          "table-row-group",
          "table-row",
          "flow-root",
          "grid",
          "inline-grid",
          "contents",
          "list-item",
          "hidden",
        ],
        float: [{ float: ["right", "left", "none", "start", "end"] }],
        clear: [{ clear: ["left", "right", "both", "none", "start", "end"] }],
        isolation: ["isolate", "isolation-auto"],
        "object-fit": [
          { object: ["contain", "cover", "fill", "none", "scale-down"] },
        ],
        "object-position": [{ object: [...H(), U] }],
        overflow: [{ overflow: N() }],
        "overflow-x": [{ "overflow-x": N() }],
        "overflow-y": [{ "overflow-y": N() }],
        overscroll: [{ overscroll: D() }],
        "overscroll-x": [{ "overscroll-x": D() }],
        "overscroll-y": [{ "overscroll-y": D() }],
        position: ["static", "fixed", "absolute", "relative", "sticky"],
        inset: [{ inset: [m] }],
        "inset-x": [{ "inset-x": [m] }],
        "inset-y": [{ "inset-y": [m] }],
        start: [{ start: [m] }],
        end: [{ end: [m] }],
        top: [{ top: [m] }],
        right: [{ right: [m] }],
        bottom: [{ bottom: [m] }],
        left: [{ left: [m] }],
        visibility: ["visible", "invisible", "collapse"],
        z: [{ z: ["auto", ki, U] }],
        basis: [{ basis: j() }],
        "flex-direction": [
          { flex: ["row", "row-reverse", "col", "col-reverse"] },
        ],
        "flex-wrap": [{ flex: ["wrap", "wrap-reverse", "nowrap"] }],
        flex: [{ flex: ["1", "auto", "initial", "none", U] }],
        grow: [{ grow: L() }],
        shrink: [{ shrink: L() }],
        order: [{ order: ["first", "last", "none", ki, U] }],
        "grid-cols": [{ "grid-cols": [Ai] }],
        "col-start-end": [{ col: ["auto", { span: ["full", ki, U] }, U] }],
        "col-start": [{ "col-start": b() }],
        "col-end": [{ "col-end": b() }],
        "grid-rows": [{ "grid-rows": [Ai] }],
        "row-start-end": [{ row: ["auto", { span: [ki, U] }, U] }],
        "row-start": [{ "row-start": b() }],
        "row-end": [{ "row-end": b() }],
        "grid-flow": [
          { "grid-flow": ["row", "col", "dense", "row-dense", "col-dense"] },
        ],
        "auto-cols": [{ "auto-cols": ["auto", "min", "max", "fr", U] }],
        "auto-rows": [{ "auto-rows": ["auto", "min", "max", "fr", U] }],
        gap: [{ gap: [f] }],
        "gap-x": [{ "gap-x": [f] }],
        "gap-y": [{ "gap-y": [f] }],
        "justify-content": [{ justify: ["normal", ...R()] }],
        "justify-items": [
          { "justify-items": ["start", "end", "center", "stretch"] },
        ],
        "justify-self": [
          { "justify-self": ["auto", "start", "end", "center", "stretch"] },
        ],
        "align-content": [{ content: ["normal", ...R(), "baseline"] }],
        "align-items": [
          { items: ["start", "end", "center", "baseline", "stretch"] },
        ],
        "align-self": [
          { self: ["auto", "start", "end", "center", "stretch", "baseline"] },
        ],
        "place-content": [{ "place-content": [...R(), "baseline"] }],
        "place-items": [
          { "place-items": ["start", "end", "center", "baseline", "stretch"] },
        ],
        "place-self": [
          { "place-self": ["auto", "start", "end", "center", "stretch"] },
        ],
        p: [{ p: [p] }],
        px: [{ px: [p] }],
        py: [{ py: [p] }],
        ps: [{ ps: [p] }],
        pe: [{ pe: [p] }],
        pt: [{ pt: [p] }],
        pr: [{ pr: [p] }],
        pb: [{ pb: [p] }],
        pl: [{ pl: [p] }],
        m: [{ m: [x] }],
        mx: [{ mx: [x] }],
        my: [{ my: [x] }],
        ms: [{ ms: [x] }],
        me: [{ me: [x] }],
        mt: [{ mt: [x] }],
        mr: [{ mr: [x] }],
        mb: [{ mb: [x] }],
        ml: [{ ml: [x] }],
        "space-x": [{ "space-x": [T] }],
        "space-x-reverse": ["space-x-reverse"],
        "space-y": [{ "space-y": [T] }],
        "space-y-reverse": ["space-y-reverse"],
        w: [{ w: ["auto", "min", "max", "fit", "svw", "lvw", "dvw", U, t] }],
        "min-w": [{ "min-w": [U, t, "min", "max", "fit"] }],
        "max-w": [
          {
            "max-w": [
              U,
              t,
              "none",
              "full",
              "min",
              "max",
              "fit",
              "prose",
              { screen: [pn] },
              pn,
            ],
          },
        ],
        h: [{ h: [U, t, "auto", "min", "max", "fit", "svh", "lvh", "dvh"] }],
        "min-h": [
          { "min-h": [U, t, "min", "max", "fit", "svh", "lvh", "dvh"] },
        ],
        "max-h": [
          { "max-h": [U, t, "min", "max", "fit", "svh", "lvh", "dvh"] },
        ],
        size: [{ size: [U, t, "auto", "min", "max", "fit"] }],
        "font-size": [{ text: ["base", pn, hn] }],
        "font-smoothing": ["antialiased", "subpixel-antialiased"],
        "font-style": ["italic", "not-italic"],
        "font-weight": [
          {
            font: [
              "thin",
              "extralight",
              "light",
              "normal",
              "medium",
              "semibold",
              "bold",
              "extrabold",
              "black",
              xl,
            ],
          },
        ],
        "font-family": [{ font: [Ai] }],
        "fvn-normal": ["normal-nums"],
        "fvn-ordinal": ["ordinal"],
        "fvn-slashed-zero": ["slashed-zero"],
        "fvn-figure": ["lining-nums", "oldstyle-nums"],
        "fvn-spacing": ["proportional-nums", "tabular-nums"],
        "fvn-fraction": ["diagonal-fractions", "stacked-fractons"],
        tracking: [
          {
            tracking: [
              "tighter",
              "tight",
              "normal",
              "wide",
              "wider",
              "widest",
              U,
            ],
          },
        ],
        "line-clamp": [{ "line-clamp": ["none", Hr, xl] }],
        leading: [
          {
            leading: [
              "none",
              "tight",
              "snug",
              "normal",
              "relaxed",
              "loose",
              Ht,
              U,
            ],
          },
        ],
        "list-image": [{ "list-image": ["none", U] }],
        "list-style-type": [{ list: ["none", "disc", "decimal", U] }],
        "list-style-position": [{ list: ["inside", "outside"] }],
        "placeholder-color": [{ placeholder: [e] }],
        "placeholder-opacity": [{ "placeholder-opacity": [h] }],
        "text-alignment": [
          { text: ["left", "center", "right", "justify", "start", "end"] },
        ],
        "text-color": [{ text: [e] }],
        "text-opacity": [{ "text-opacity": [h] }],
        "text-decoration": [
          "underline",
          "overline",
          "line-through",
          "no-underline",
        ],
        "text-decoration-style": [{ decoration: [...G(), "wavy"] }],
        "text-decoration-thickness": [
          { decoration: ["auto", "from-font", Ht, hn] },
        ],
        "underline-offset": [{ "underline-offset": ["auto", Ht, U] }],
        "text-decoration-color": [{ decoration: [e] }],
        "text-transform": [
          "uppercase",
          "lowercase",
          "capitalize",
          "normal-case",
        ],
        "text-overflow": ["truncate", "text-ellipsis", "text-clip"],
        "text-wrap": [{ text: ["wrap", "nowrap", "balance", "pretty"] }],
        indent: [{ indent: I() }],
        "vertical-align": [
          {
            align: [
              "baseline",
              "top",
              "middle",
              "bottom",
              "text-top",
              "text-bottom",
              "sub",
              "super",
              U,
            ],
          },
        ],
        whitespace: [
          {
            whitespace: [
              "normal",
              "nowrap",
              "pre",
              "pre-line",
              "pre-wrap",
              "break-spaces",
            ],
          },
        ],
        break: [{ break: ["normal", "words", "all", "keep"] }],
        hyphens: [{ hyphens: ["none", "manual", "auto"] }],
        content: [{ content: ["none", U] }],
        "bg-attachment": [{ bg: ["fixed", "local", "scroll"] }],
        "bg-clip": [{ "bg-clip": ["border", "padding", "content", "text"] }],
        "bg-opacity": [{ "bg-opacity": [h] }],
        "bg-origin": [{ "bg-origin": ["border", "padding", "content"] }],
        "bg-position": [{ bg: [...H(), hC] }],
        "bg-repeat": [
          { bg: ["no-repeat", { repeat: ["", "x", "y", "round", "space"] }] },
        ],
        "bg-size": [{ bg: ["auto", "cover", "contain", fC] }],
        "bg-image": [
          {
            bg: [
              "none",
              { "gradient-to": ["t", "tr", "r", "br", "b", "bl", "l", "tl"] },
              mC,
            ],
          },
        ],
        "bg-color": [{ bg: [e] }],
        "gradient-from-pos": [{ from: [y] }],
        "gradient-via-pos": [{ via: [y] }],
        "gradient-to-pos": [{ to: [y] }],
        "gradient-from": [{ from: [v] }],
        "gradient-via": [{ via: [v] }],
        "gradient-to": [{ to: [v] }],
        rounded: [{ rounded: [s] }],
        "rounded-s": [{ "rounded-s": [s] }],
        "rounded-e": [{ "rounded-e": [s] }],
        "rounded-t": [{ "rounded-t": [s] }],
        "rounded-r": [{ "rounded-r": [s] }],
        "rounded-b": [{ "rounded-b": [s] }],
        "rounded-l": [{ "rounded-l": [s] }],
        "rounded-ss": [{ "rounded-ss": [s] }],
        "rounded-se": [{ "rounded-se": [s] }],
        "rounded-ee": [{ "rounded-ee": [s] }],
        "rounded-es": [{ "rounded-es": [s] }],
        "rounded-tl": [{ "rounded-tl": [s] }],
        "rounded-tr": [{ "rounded-tr": [s] }],
        "rounded-br": [{ "rounded-br": [s] }],
        "rounded-bl": [{ "rounded-bl": [s] }],
        "border-w": [{ border: [a] }],
        "border-w-x": [{ "border-x": [a] }],
        "border-w-y": [{ "border-y": [a] }],
        "border-w-s": [{ "border-s": [a] }],
        "border-w-e": [{ "border-e": [a] }],
        "border-w-t": [{ "border-t": [a] }],
        "border-w-r": [{ "border-r": [a] }],
        "border-w-b": [{ "border-b": [a] }],
        "border-w-l": [{ "border-l": [a] }],
        "border-opacity": [{ "border-opacity": [h] }],
        "border-style": [{ border: [...G(), "hidden"] }],
        "divide-x": [{ "divide-x": [a] }],
        "divide-x-reverse": ["divide-x-reverse"],
        "divide-y": [{ "divide-y": [a] }],
        "divide-y-reverse": ["divide-y-reverse"],
        "divide-opacity": [{ "divide-opacity": [h] }],
        "divide-style": [{ divide: G() }],
        "border-color": [{ border: [i] }],
        "border-color-x": [{ "border-x": [i] }],
        "border-color-y": [{ "border-y": [i] }],
        "border-color-s": [{ "border-s": [i] }],
        "border-color-e": [{ "border-e": [i] }],
        "border-color-t": [{ "border-t": [i] }],
        "border-color-r": [{ "border-r": [i] }],
        "border-color-b": [{ "border-b": [i] }],
        "border-color-l": [{ "border-l": [i] }],
        "divide-color": [{ divide: [i] }],
        "outline-style": [{ outline: ["", ...G()] }],
        "outline-offset": [{ "outline-offset": [Ht, U] }],
        "outline-w": [{ outline: [Ht, hn] }],
        "outline-color": [{ outline: [e] }],
        "ring-w": [{ ring: Z() }],
        "ring-w-inset": ["ring-inset"],
        "ring-color": [{ ring: [e] }],
        "ring-opacity": [{ "ring-opacity": [h] }],
        "ring-offset-w": [{ "ring-offset": [Ht, hn] }],
        "ring-offset-color": [{ "ring-offset": [e] }],
        shadow: [{ shadow: ["", "inner", "none", pn, gC] }],
        "shadow-color": [{ shadow: [Ai] }],
        opacity: [{ opacity: [h] }],
        "mix-blend": [{ "mix-blend": [...B(), "plus-lighter", "plus-darker"] }],
        "bg-blend": [{ "bg-blend": B() }],
        filter: [{ filter: ["", "none"] }],
        blur: [{ blur: [n] }],
        brightness: [{ brightness: [r] }],
        contrast: [{ contrast: [l] }],
        "drop-shadow": [{ "drop-shadow": ["", "none", pn, U] }],
        grayscale: [{ grayscale: [u] }],
        "hue-rotate": [{ "hue-rotate": [c] }],
        invert: [{ invert: [d] }],
        saturate: [{ saturate: [g] }],
        sepia: [{ sepia: [C] }],
        "backdrop-filter": [{ "backdrop-filter": ["", "none"] }],
        "backdrop-blur": [{ "backdrop-blur": [n] }],
        "backdrop-brightness": [{ "backdrop-brightness": [r] }],
        "backdrop-contrast": [{ "backdrop-contrast": [l] }],
        "backdrop-grayscale": [{ "backdrop-grayscale": [u] }],
        "backdrop-hue-rotate": [{ "backdrop-hue-rotate": [c] }],
        "backdrop-invert": [{ "backdrop-invert": [d] }],
        "backdrop-opacity": [{ "backdrop-opacity": [h] }],
        "backdrop-saturate": [{ "backdrop-saturate": [g] }],
        "backdrop-sepia": [{ "backdrop-sepia": [C] }],
        "border-collapse": [{ border: ["collapse", "separate"] }],
        "border-spacing": [{ "border-spacing": [o] }],
        "border-spacing-x": [{ "border-spacing-x": [o] }],
        "border-spacing-y": [{ "border-spacing-y": [o] }],
        "table-layout": [{ table: ["auto", "fixed"] }],
        caption: [{ caption: ["top", "bottom"] }],
        transition: [
          {
            transition: [
              "none",
              "all",
              "",
              "colors",
              "opacity",
              "shadow",
              "transform",
              U,
            ],
          },
        ],
        duration: [{ duration: z() }],
        ease: [{ ease: ["linear", "in", "out", "in-out", U] }],
        delay: [{ delay: z() }],
        animate: [{ animate: ["none", "spin", "ping", "pulse", "bounce", U] }],
        transform: [{ transform: ["", "gpu", "none"] }],
        scale: [{ scale: [S] }],
        "scale-x": [{ "scale-x": [S] }],
        "scale-y": [{ "scale-y": [S] }],
        rotate: [{ rotate: [ki, U] }],
        "translate-x": [{ "translate-x": [E] }],
        "translate-y": [{ "translate-y": [E] }],
        "skew-x": [{ "skew-x": [k] }],
        "skew-y": [{ "skew-y": [k] }],
        "transform-origin": [
          {
            origin: [
              "center",
              "top",
              "top-right",
              "right",
              "bottom-right",
              "bottom",
              "bottom-left",
              "left",
              "top-left",
              U,
            ],
          },
        ],
        accent: [{ accent: ["auto", e] }],
        appearance: [{ appearance: ["none", "auto"] }],
        cursor: [
          {
            cursor: [
              "auto",
              "default",
              "pointer",
              "wait",
              "text",
              "move",
              "help",
              "not-allowed",
              "none",
              "context-menu",
              "progress",
              "cell",
              "crosshair",
              "vertical-text",
              "alias",
              "copy",
              "no-drop",
              "grab",
              "grabbing",
              "all-scroll",
              "col-resize",
              "row-resize",
              "n-resize",
              "e-resize",
              "s-resize",
              "w-resize",
              "ne-resize",
              "nw-resize",
              "se-resize",
              "sw-resize",
              "ew-resize",
              "ns-resize",
              "nesw-resize",
              "nwse-resize",
              "zoom-in",
              "zoom-out",
              U,
            ],
          },
        ],
        "caret-color": [{ caret: [e] }],
        "pointer-events": [{ "pointer-events": ["none", "auto"] }],
        resize: [{ resize: ["none", "y", "x", ""] }],
        "scroll-behavior": [{ scroll: ["auto", "smooth"] }],
        "scroll-m": [{ "scroll-m": I() }],
        "scroll-mx": [{ "scroll-mx": I() }],
        "scroll-my": [{ "scroll-my": I() }],
        "scroll-ms": [{ "scroll-ms": I() }],
        "scroll-me": [{ "scroll-me": I() }],
        "scroll-mt": [{ "scroll-mt": I() }],
        "scroll-mr": [{ "scroll-mr": I() }],
        "scroll-mb": [{ "scroll-mb": I() }],
        "scroll-ml": [{ "scroll-ml": I() }],
        "scroll-p": [{ "scroll-p": I() }],
        "scroll-px": [{ "scroll-px": I() }],
        "scroll-py": [{ "scroll-py": I() }],
        "scroll-ps": [{ "scroll-ps": I() }],
        "scroll-pe": [{ "scroll-pe": I() }],
        "scroll-pt": [{ "scroll-pt": I() }],
        "scroll-pr": [{ "scroll-pr": I() }],
        "scroll-pb": [{ "scroll-pb": I() }],
        "scroll-pl": [{ "scroll-pl": I() }],
        "snap-align": [{ snap: ["start", "end", "center", "align-none"] }],
        "snap-stop": [{ snap: ["normal", "always"] }],
        "snap-type": [{ snap: ["none", "x", "y", "both"] }],
        "snap-strictness": [{ snap: ["mandatory", "proximity"] }],
        touch: [{ touch: ["auto", "none", "manipulation"] }],
        "touch-x": [{ "touch-pan": ["x", "left", "right"] }],
        "touch-y": [{ "touch-pan": ["y", "up", "down"] }],
        "touch-pz": ["touch-pinch-zoom"],
        select: [{ select: ["none", "text", "all", "auto"] }],
        "will-change": [
          { "will-change": ["auto", "scroll", "contents", "transform", U] },
        ],
        fill: [{ fill: [e, "none"] }],
        "stroke-w": [{ stroke: [Ht, hn, xl] }],
        stroke: [{ stroke: [e, "none"] }],
        sr: ["sr-only", "not-sr-only"],
        "forced-color-adjust": [{ "forced-color-adjust": ["auto", "none"] }],
      },
      conflictingClassGroups: {
        overflow: ["overflow-x", "overflow-y"],
        overscroll: ["overscroll-x", "overscroll-y"],
        inset: [
          "inset-x",
          "inset-y",
          "start",
          "end",
          "top",
          "right",
          "bottom",
          "left",
        ],
        "inset-x": ["right", "left"],
        "inset-y": ["top", "bottom"],
        flex: ["basis", "grow", "shrink"],
        gap: ["gap-x", "gap-y"],
        p: ["px", "py", "ps", "pe", "pt", "pr", "pb", "pl"],
        px: ["pr", "pl"],
        py: ["pt", "pb"],
        m: ["mx", "my", "ms", "me", "mt", "mr", "mb", "ml"],
        mx: ["mr", "ml"],
        my: ["mt", "mb"],
        size: ["w", "h"],
        "font-size": ["leading"],
        "fvn-normal": [
          "fvn-ordinal",
          "fvn-slashed-zero",
          "fvn-figure",
          "fvn-spacing",
          "fvn-fraction",
        ],
        "fvn-ordinal": ["fvn-normal"],
        "fvn-slashed-zero": ["fvn-normal"],
        "fvn-figure": ["fvn-normal"],
        "fvn-spacing": ["fvn-normal"],
        "fvn-fraction": ["fvn-normal"],
        "line-clamp": ["display", "overflow"],
        rounded: [
          "rounded-s",
          "rounded-e",
          "rounded-t",
          "rounded-r",
          "rounded-b",
          "rounded-l",
          "rounded-ss",
          "rounded-se",
          "rounded-ee",
          "rounded-es",
          "rounded-tl",
          "rounded-tr",
          "rounded-br",
          "rounded-bl",
        ],
        "rounded-s": ["rounded-ss", "rounded-es"],
        "rounded-e": ["rounded-se", "rounded-ee"],
        "rounded-t": ["rounded-tl", "rounded-tr"],
        "rounded-r": ["rounded-tr", "rounded-br"],
        "rounded-b": ["rounded-br", "rounded-bl"],
        "rounded-l": ["rounded-tl", "rounded-bl"],
        "border-spacing": ["border-spacing-x", "border-spacing-y"],
        "border-w": [
          "border-w-s",
          "border-w-e",
          "border-w-t",
          "border-w-r",
          "border-w-b",
          "border-w-l",
        ],
        "border-w-x": ["border-w-r", "border-w-l"],
        "border-w-y": ["border-w-t", "border-w-b"],
        "border-color": [
          "border-color-s",
          "border-color-e",
          "border-color-t",
          "border-color-r",
          "border-color-b",
          "border-color-l",
        ],
        "border-color-x": ["border-color-r", "border-color-l"],
        "border-color-y": ["border-color-t", "border-color-b"],
        "scroll-m": [
          "scroll-mx",
          "scroll-my",
          "scroll-ms",
          "scroll-me",
          "scroll-mt",
          "scroll-mr",
          "scroll-mb",
          "scroll-ml",
        ],
        "scroll-mx": ["scroll-mr", "scroll-ml"],
        "scroll-my": ["scroll-mt", "scroll-mb"],
        "scroll-p": [
          "scroll-px",
          "scroll-py",
          "scroll-ps",
          "scroll-pe",
          "scroll-pt",
          "scroll-pr",
          "scroll-pb",
          "scroll-pl",
        ],
        "scroll-px": ["scroll-pr", "scroll-pl"],
        "scroll-py": ["scroll-pt", "scroll-pb"],
        touch: ["touch-x", "touch-y", "touch-pz"],
        "touch-x": ["touch"],
        "touch-y": ["touch"],
        "touch-pz": ["touch"],
      },
      conflictingClassGroupModifiers: { "font-size": ["leading"] },
    };
  },
  SC = nC(wC);
function at(...e) {
  return SC($P(e));
}
const PC = RP,
  uv = w.forwardRef(({ className: e, ...t }, n) =>
    P.jsx(Ky, {
      ref: n,
      className: at(
        "fixed top-0 z-[100] flex max-h-screen w-full flex-col-reverse p-4 sm:bottom-0 sm:right-0 sm:top-auto sm:flex-col md:max-w-[420px]",
        e
      ),
      ...t,
    })
  );
uv.displayName = Ky.displayName;
const CC = Jy(
    "group pointer-events-auto relative flex w-full items-center justify-between space-x-4 overflow-hidden rounded-md border p-6 pr-8 shadow-lg transition-all data-[swipe=cancel]:translate-x-0 data-[swipe=end]:translate-x-[var(--radix-toast-swipe-end-x)] data-[swipe=move]:translate-x-[var(--radix-toast-swipe-move-x)] data-[swipe=move]:transition-none data-[state=open]:animate-in data-[state=closed]:animate-out data-[swipe=end]:animate-out data-[state=closed]:fade-out-80 data-[state=closed]:slide-out-to-right-full data-[state=open]:slide-in-from-top-full data-[state=open]:sm:slide-in-from-bottom-full",
    {
      variants: {
        variant: {
          default: "border bg-background text-foreground",
          destructive:
            "destructive group border-destructive bg-destructive text-destructive-foreground",
        },
      },
      defaultVariants: { variant: "default" },
    }
  ),
  cv = w.forwardRef(({ className: e, variant: t, ...n }, r) =>
    P.jsx(Qy, { ref: r, className: at(CC({ variant: t }), e), ...n })
  );
cv.displayName = Qy.displayName;
const EC = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx(Xy, {
    ref: n,
    className: at(
      "inline-flex h-8 shrink-0 items-center justify-center rounded-md border bg-transparent px-3 text-sm font-medium ring-offset-background transition-colors hover:bg-secondary focus:outline-none focus:ring-2 focus:ring-ring focus:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 group-[.destructive]:border-muted/40 group-[.destructive]:hover:border-destructive/30 group-[.destructive]:hover:bg-destructive group-[.destructive]:hover:text-destructive-foreground group-[.destructive]:focus:ring-destructive",
      e
    ),
    ...t,
  })
);
EC.displayName = Xy.displayName;
const dv = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx(Yy, {
    ref: n,
    className: at(
      "absolute right-2 top-2 rounded-md p-1 text-foreground/50 opacity-0 transition-opacity hover:text-foreground focus:opacity-100 focus:outline-none focus:ring-2 group-hover:opacity-100 group-[.destructive]:text-red-300 group-[.destructive]:hover:text-red-50 group-[.destructive]:focus:ring-red-400 group-[.destructive]:focus:ring-offset-red-600",
      e
    ),
    "toast-close": "",
    ...t,
    children: P.jsx(nv, { className: "h-4 w-4" }),
  })
);
dv.displayName = Yy.displayName;
const fv = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx(Gy, { ref: n, className: at("text-sm font-semibold", e), ...t })
);
fv.displayName = Gy.displayName;
const hv = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx(qy, { ref: n, className: at("text-sm opacity-90", e), ...t })
);
hv.displayName = qy.displayName;
function TC() {
  const { toasts: e } = FS();
  return P.jsxs(PC, {
    children: [
      e.map(function ({ id: t, title: n, description: r, action: i, ...s }) {
        return P.jsxs(
          cv,
          {
            ...s,
            children: [
              P.jsxs("div", {
                className: "grid gap-1",
                children: [
                  n && P.jsx(fv, { children: n }),
                  r && P.jsx(hv, { children: r }),
                ],
              }),
              i,
              P.jsx(dv, {}),
            ],
          },
          t
        );
      }),
      P.jsx(uv, {}),
    ],
  });
}
const Aa = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx("div", {
    ref: n,
    className: at(
      "rounded-lg border bg-card text-card-foreground shadow-sm",
      e
    ),
    ...t,
  })
);
Aa.displayName = "Card";
const pv = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx("div", {
    ref: n,
    className: at("flex flex-col space-y-1.5 p-6", e),
    ...t,
  })
);
pv.displayName = "CardHeader";
const mv = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx("h3", {
    ref: n,
    className: at("text-2xl font-semibold leading-none tracking-tight", e),
    ...t,
  })
);
mv.displayName = "CardTitle";
const kC = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx("p", {
    ref: n,
    className: at("text-sm text-muted-foreground", e),
    ...t,
  })
);
kC.displayName = "CardDescription";
const Ra = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx("div", { ref: n, className: at("p-6 pt-0", e), ...t })
);
Ra.displayName = "CardContent";
const AC = w.forwardRef(({ className: e, ...t }, n) =>
  P.jsx("div", { ref: n, className: at("flex items-center p-6 pt-0", e), ...t })
);
AC.displayName = "CardFooter";
function RC() {
  return P.jsx("div", {
    className:
      "min-h-screen w-full flex items-center justify-center bg-gray-50",
    children: P.jsx(Aa, {
      className: "w-full max-w-md mx-4",
      children: P.jsxs(Ra, {
        className: "pt-6",
        children: [
          P.jsxs("div", {
            className: "flex mb-4 gap-2",
            children: [
              P.jsx(jP, { className: "h-8 w-8 text-red-500" }),
              P.jsx("h1", {
                className: "text-2xl font-bold text-gray-900",
                children: "404 Page Not Found",
              }),
            ],
          }),
          P.jsx("p", {
            className: "mt-4 text-sm text-gray-600",
            children: "Did you forget to add the page to the router?",
          }),
        ],
      }),
    }),
  });
}
const MC = Jy(
    "inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-md text-sm font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 [&_svg]:pointer-events-none [&_svg]:size-4 [&_svg]:shrink-0",
    {
      variants: {
        variant: {
          default: "bg-primary text-primary-foreground hover:bg-primary/90",
          destructive:
            "bg-destructive text-destructive-foreground hover:bg-destructive/90",
          outline:
            "border border-input bg-background hover:bg-accent hover:text-accent-foreground",
          secondary:
            "bg-secondary text-secondary-foreground hover:bg-secondary/80",
          ghost: "hover:bg-accent hover:text-accent-foreground",
          link: "text-primary underline-offset-4 hover:underline",
        },
        size: {
          default: "h-10 px-4 py-2",
          sm: "h-9 rounded-md px-3",
          lg: "h-11 rounded-md px-8",
          icon: "h-10 w-10",
        },
      },
      defaultVariants: { variant: "default", size: "default" },
    }
  ),
  nr = w.forwardRef(
    ({ className: e, variant: t, size: n, asChild: r = !1, ...i }, s) => {
      const o = r ? ms : "button";
      return P.jsx(o, {
        className: at(MC({ variant: t, size: n, className: e })),
        ref: s,
        ...i,
      });
    }
  );
nr.displayName = "Button";
function DC() {
  const [e, t] = w.useState(!1),
    n = [
      { href: "#services", label: "Services" },
      { href: "#certifications", label: "Certifications" },
      { href: "#contact", label: "Contact" },
    ];
  return P.jsxs(P.Fragment, {
    children: [
      P.jsx("nav", {
        className: "fixed w-full bg-background/95 backdrop-blur z-50 border-b",
        children: P.jsxs("div", {
          className: "container mx-auto px-4",
          children: [
            P.jsxs("div", {
              className: "flex items-center justify-between h-16",
              children: [
                P.jsx(rS, {
                  href: "/",
                  children: P.jsx("span", {
                    className: "text-xl font-bold text-primary",
                    children: "Aerospace Seal & Diaphragm MRO",
                  }),
                }),
                P.jsxs("div", {
                  className: "hidden md:flex items-center space-x-8",
                  children: [
                    n.map((r) =>
                      P.jsx(
                        "a",
                        {
                          href: r.href,
                          className:
                            "text-foreground/80 hover:text-primary transition-colors flex items-center h-16",
                          children: r.label,
                        },
                        r.href
                      )
                    ),
                    P.jsx(nr, {
                      asChild: !0,
                      children: P.jsx("a", {
                        href: "mailto:rfq@asdmro.com?subject=ASD%20MRO%20RFQ",
                        children: "Request Quote",
                      }),
                    }),
                  ],
                }),
                P.jsx("button", {
                  className: "md:hidden",
                  onClick: () => t(!e),
                  children: e
                    ? P.jsx(nv, { className: "h-6 w-6" })
                    : P.jsx(VP, { className: "h-6 w-6" }),
                }),
              ],
            }),
            e &&
              P.jsx("div", {
                className: "md:hidden py-4",
                children: P.jsxs("div", {
                  className: "flex flex-col space-y-4",
                  children: [
                    n.map((r) =>
                      P.jsx(
                        "a",
                        {
                          href: r.href,
                          className:
                            "text-foreground/80 hover:text-primary transition-colors",
                          onClick: () => t(!1),
                          children: r.label,
                        },
                        r.href
                      )
                    ),
                    P.jsx(nr, {
                      asChild: !0,
                      children: P.jsx("a", {
                        href: "mailto:rfq@asdmro.com?subject=ASD%20MRO%20RFQ",
                        children: "Request Quote",
                      }),
                    }),
                  ],
                }),
              }),
          ],
        }),
      }),
      P.jsx("div", {
        className:
          "fixed top-16 w-full bg-primary text-white py-1.5 z-40 text-center",
        children: P.jsxs("div", {
          className: "container mx-auto px-4 text-sm",
          children: [
            "Looking for build-to-print aerospace manufacturing services? Please visit our sibling company,",
            " ",
            P.jsx("a", {
              href: "http://www.micro-tronics.com",
              target: "_blank",
              rel: "noopener noreferrer",
              className: "font-bold hover:underline",
              children: "www.micro-tronics.com",
            }),
          ],
        }),
      }),
      P.jsx("div", { className: "h-28" }),
    ],
  });
}
function NC() {
  return P.jsx("footer", {
    className: "bg-gray-900 text-gray-300",
    children: P.jsxs("div", {
      className: "container mx-auto px-4 py-12",
      children: [
        P.jsxs("div", {
          className: "grid md:grid-cols-3 gap-8",
          children: [
            P.jsxs("div", {
              children: [
                P.jsx("h3", {
                  className: "text-white font-bold text-lg mb-4",
                  children: "Aerospace Seal & Diaphragm MRO",
                }),
                P.jsx("p", {
                  className: "text-gray-400",
                  children:
                    "Specialized re-molding of aerospace plate seals, R&O services for diaphragms, diaphragm assemblies, and other elastomer components. Industry-leading quality and rapid turnaround times.",
                }),
                P.jsx("p", {
                  className: "text-gray-400 mt-2",
                  children:
                    "Serving airline, OEM, MRO, and military customers.",
                }),
              ],
            }),
            P.jsxs("div", {
              children: [
                P.jsx("h3", {
                  className: "text-white font-bold text-lg mb-4",
                  children: "Contact",
                }),
                P.jsxs("div", {
                  className: "space-y-3",
                  children: [
                    P.jsxs("div", {
                      className: "flex items-center gap-2",
                      children: [
                        P.jsx(zP, { className: "h-5 w-5" }),
                        P.jsx("span", { children: "(602) 437-8995" }),
                      ],
                    }),
                    P.jsxs("div", {
                      className: "flex items-center gap-2",
                      children: [
                        P.jsx(FP, { className: "h-5 w-5" }),
                        P.jsx("span", { children: "rfq@asdmro.com" }),
                      ],
                    }),
                    P.jsxs("div", {
                      className: "flex items-center gap-2",
                      children: [
                        P.jsx(_P, { className: "h-5 w-5" }),
                        P.jsx("span", {
                          children: "2906 S 52nd St, Tempe, AZ 85282",
                        }),
                      ],
                    }),
                  ],
                }),
              ],
            }),
            P.jsxs("div", {
              children: [
                P.jsx("h3", {
                  className: "text-white font-bold text-lg mb-4",
                  children: "Certifications",
                }),
                P.jsxs("ul", {
                  className: "space-y-2",
                  children: [
                    P.jsx("li", { children: "AS9100D Certified" }),
                    P.jsx("li", { children: "ISO 9001:2015" }),
                    P.jsx("li", { children: "NADCAP - Elastomer Seals" }),
                    P.jsx("li", { children: "FAA Part 145" }),
                    P.jsx("li", { children: "EASA" }),
                    P.jsx("li", {
                      children:
                        "Anti-Drug and Alcohol Misuse Prevention Program",
                    }),
                  ],
                }),
              ],
            }),
          ],
        }),
        P.jsx("div", {
          className: "border-t border-gray-800 mt-8 pt-8 text-center",
          children: P.jsxs("p", {
            children: [
              "Â© ",
              new Date().getFullYear(),
              " Aerospace Seal & Diaphragm MRO. All rights reserved.",
            ],
          }),
        }),
      ],
    }),
  });
}
function bC(e) {
  if (typeof Proxy > "u") return e;
  const t = new Map(),
    n = (...r) => e(...r);
  return new Proxy(n, {
    get: (r, i) =>
      i === "create" ? e : (t.has(i) || t.set(i, e(i)), t.get(i)),
  });
}
function Ma(e) {
  return e !== null && typeof e == "object" && typeof e.start == "function";
}
const bu = (e) => Array.isArray(e);
function gv(e, t) {
  if (!Array.isArray(t)) return !1;
  const n = t.length;
  if (n !== e.length) return !1;
  for (let r = 0; r < n; r++) if (t[r] !== e[r]) return !1;
  return !0;
}
function gs(e) {
  return typeof e == "string" || Array.isArray(e);
}
function Eh(e) {
  const t = [{}, {}];
  return (
    e == null ||
      e.values.forEach((n, r) => {
        (t[0][r] = n.get()), (t[1][r] = n.getVelocity());
      }),
    t
  );
}
function td(e, t, n, r) {
  if (typeof t == "function") {
    const [i, s] = Eh(r);
    t = t(n !== void 0 ? n : e.custom, i, s);
  }
  if (
    (typeof t == "string" && (t = e.variants && e.variants[t]),
    typeof t == "function")
  ) {
    const [i, s] = Eh(r);
    t = t(n !== void 0 ? n : e.custom, i, s);
  }
  return t;
}
function Da(e, t, n) {
  const r = e.getProps();
  return td(r, t, n !== void 0 ? n : r.custom, e);
}
const nd = [
    "animate",
    "whileInView",
    "whileFocus",
    "whileHover",
    "whileTap",
    "whileDrag",
    "exit",
  ],
  rd = ["initial", ...nd],
  Ds = [
    "transformPerspective",
    "x",
    "y",
    "z",
    "translateX",
    "translateY",
    "translateZ",
    "scale",
    "scaleX",
    "scaleY",
    "rotate",
    "rotateX",
    "rotateY",
    "rotateZ",
    "skew",
    "skewX",
    "skewY",
  ],
  wr = new Set(Ds),
  Jt = (e) => e * 1e3,
  en = (e) => e / 1e3,
  LC = { type: "spring", stiffness: 500, damping: 25, restSpeed: 10 },
  OC = (e) => ({
    type: "spring",
    stiffness: 550,
    damping: e === 0 ? 2 * Math.sqrt(550) : 30,
    restSpeed: 10,
  }),
  jC = { type: "keyframes", duration: 0.8 },
  IC = { type: "keyframes", ease: [0.25, 0.1, 0.35, 1], duration: 0.3 },
  FC = (e, { keyframes: t }) =>
    t.length > 2
      ? jC
      : wr.has(e)
      ? e.startsWith("scale")
        ? OC(t[1])
        : LC
      : IC;
function id(e, t) {
  return e ? e[t] || e.default || e : void 0;
}
const _C = { skipAnimations: !1, useManualTiming: !1 },
  VC = (e) => e !== null;
function Na(e, { repeat: t, repeatType: n = "loop" }, r) {
  const i = e.filter(VC),
    s = t && n !== "loop" && t % 2 === 1 ? 0 : i.length - 1;
  return !s || r === void 0 ? i[s] : r;
}
const Ie = (e) => e;
let Lu = Ie;
function zC(e) {
  let t = new Set(),
    n = new Set(),
    r = !1,
    i = !1;
  const s = new WeakSet();
  let o = { delta: 0, timestamp: 0, isProcessing: !1 };
  function a(u) {
    s.has(u) && (l.schedule(u), e()), u(o);
  }
  const l = {
    schedule: (u, c = !1, d = !1) => {
      const v = d && r ? t : n;
      return c && s.add(u), v.has(u) || v.add(u), u;
    },
    cancel: (u) => {
      n.delete(u), s.delete(u);
    },
    process: (u) => {
      if (((o = u), r)) {
        i = !0;
        return;
      }
      (r = !0),
        ([t, n] = [n, t]),
        n.clear(),
        t.forEach(a),
        (r = !1),
        i && ((i = !1), l.process(u));
    },
  };
  return l;
}
const ro = [
    "read",
    "resolveKeyframes",
    "update",
    "preRender",
    "render",
    "postRender",
  ],
  BC = 40;
function yv(e, t) {
  let n = !1,
    r = !0;
  const i = { delta: 0, timestamp: 0, isProcessing: !1 },
    s = () => (n = !0),
    o = ro.reduce((h, p) => ((h[p] = zC(s)), h), {}),
    {
      read: a,
      resolveKeyframes: l,
      update: u,
      preRender: c,
      render: d,
      postRender: f,
    } = o,
    v = () => {
      const h = performance.now();
      (n = !1),
        (i.delta = r ? 1e3 / 60 : Math.max(Math.min(h - i.timestamp, BC), 1)),
        (i.timestamp = h),
        (i.isProcessing = !0),
        a.process(i),
        l.process(i),
        u.process(i),
        c.process(i),
        d.process(i),
        f.process(i),
        (i.isProcessing = !1),
        n && t && ((r = !1), e(v));
    },
    y = () => {
      (n = !0), (r = !0), i.isProcessing || e(v);
    };
  return {
    schedule: ro.reduce((h, p) => {
      const g = o[p];
      return (h[p] = (S, C = !1, k = !1) => (n || y(), g.schedule(S, C, k))), h;
    }, {}),
    cancel: (h) => {
      for (let p = 0; p < ro.length; p++) o[ro[p]].cancel(h);
    },
    state: i,
    steps: o,
  };
}
const {
    schedule: Y,
    cancel: Bn,
    state: ke,
    steps: wl,
  } = yv(typeof requestAnimationFrame < "u" ? requestAnimationFrame : Ie, !0),
  vv = (e, t, n) =>
    (((1 - 3 * n + 3 * t) * e + (3 * n - 6 * t)) * e + 3 * t) * e,
  UC = 1e-7,
  $C = 12;
function WC(e, t, n, r, i) {
  let s,
    o,
    a = 0;
  do (o = t + (n - t) / 2), (s = vv(o, r, i) - e), s > 0 ? (n = o) : (t = o);
  while (Math.abs(s) > UC && ++a < $C);
  return o;
}
function Ns(e, t, n, r) {
  if (e === t && n === r) return Ie;
  const i = (s) => WC(s, 0, 1, e, n);
  return (s) => (s === 0 || s === 1 ? s : vv(i(s), t, r));
}
const xv = (e) => (t) => t <= 0.5 ? e(2 * t) / 2 : (2 - e(2 * (1 - t))) / 2,
  wv = (e) => (t) => 1 - e(1 - t),
  Sv = Ns(0.33, 1.53, 0.69, 0.99),
  sd = wv(Sv),
  Pv = xv(sd),
  Cv = (e) =>
    (e *= 2) < 1 ? 0.5 * sd(e) : 0.5 * (2 - Math.pow(2, -10 * (e - 1))),
  od = (e) => 1 - Math.sin(Math.acos(e)),
  Ev = wv(od),
  Tv = xv(od),
  kv = (e) => /^0[^.\s]+$/u.test(e);
function HC(e) {
  return typeof e == "number"
    ? e === 0
    : e !== null
    ? e === "none" || e === "0" || kv(e)
    : !0;
}
const Av = (e) => /^-?(?:\d+(?:\.\d+)?|\.\d+)$/u.test(e),
  Rv = (e) => (t) => typeof t == "string" && t.startsWith(e),
  Mv = Rv("--"),
  KC = Rv("var(--"),
  ad = (e) => (KC(e) ? QC.test(e.split("/*")[0].trim()) : !1),
  QC =
    /var\(--(?:[\w-]+\s*|[\w-]+\s*,(?:\s*[^)(\s]|\s*\((?:[^)(]|\([^)(]*\))*\))+\s*)\)$/iu,
  GC = /^var\(--(?:([\w-]+)|([\w-]+), ?([a-zA-Z\d ()%#.,-]+))\)/u;
function qC(e) {
  const t = GC.exec(e);
  if (!t) return [,];
  const [, n, r, i] = t;
  return [`--${n ?? r}`, i];
}
function Dv(e, t, n = 1) {
  const [r, i] = qC(e);
  if (!r) return;
  const s = window.getComputedStyle(t).getPropertyValue(r);
  if (s) {
    const o = s.trim();
    return Av(o) ? parseFloat(o) : o;
  }
  return ad(i) ? Dv(i, t, n + 1) : i;
}
const an = (e, t, n) => (n > t ? t : n < e ? e : n),
  gi = {
    test: (e) => typeof e == "number",
    parse: parseFloat,
    transform: (e) => e,
  },
  ys = { ...gi, transform: (e) => an(0, 1, e) },
  io = { ...gi, default: 1 },
  bs = (e) => ({
    test: (t) =>
      typeof t == "string" && t.endsWith(e) && t.split(" ").length === 1,
    parse: parseFloat,
    transform: (t) => `${t}${e}`,
  }),
  yn = bs("deg"),
  Vt = bs("%"),
  V = bs("px"),
  XC = bs("vh"),
  YC = bs("vw"),
  Th = {
    ...Vt,
    parse: (e) => Vt.parse(e) / 100,
    transform: (e) => Vt.transform(e * 100),
  },
  ZC = new Set([
    "width",
    "height",
    "top",
    "left",
    "right",
    "bottom",
    "x",
    "y",
    "translateX",
    "translateY",
  ]),
  kh = (e) => e === gi || e === V,
  Ah = (e, t) => parseFloat(e.split(", ")[t]),
  Rh =
    (e, t) =>
    (n, { transform: r }) => {
      if (r === "none" || !r) return 0;
      const i = r.match(/^matrix3d\((.+)\)$/u);
      if (i) return Ah(i[1], t);
      {
        const s = r.match(/^matrix\((.+)\)$/u);
        return s ? Ah(s[1], e) : 0;
      }
    },
  JC = new Set(["x", "y", "z"]),
  eE = Ds.filter((e) => !JC.has(e));
function tE(e) {
  const t = [];
  return (
    eE.forEach((n) => {
      const r = e.getValue(n);
      r !== void 0 &&
        (t.push([n, r.get()]), r.set(n.startsWith("scale") ? 1 : 0));
    }),
    t
  );
}
const ui = {
  width: ({ x: e }, { paddingLeft: t = "0", paddingRight: n = "0" }) =>
    e.max - e.min - parseFloat(t) - parseFloat(n),
  height: ({ y: e }, { paddingTop: t = "0", paddingBottom: n = "0" }) =>
    e.max - e.min - parseFloat(t) - parseFloat(n),
  top: (e, { top: t }) => parseFloat(t),
  left: (e, { left: t }) => parseFloat(t),
  bottom: ({ y: e }, { top: t }) => parseFloat(t) + (e.max - e.min),
  right: ({ x: e }, { left: t }) => parseFloat(t) + (e.max - e.min),
  x: Rh(4, 13),
  y: Rh(5, 14),
};
ui.translateX = ui.x;
ui.translateY = ui.y;
const Nv = (e) => (t) => t.test(e),
  nE = { test: (e) => e === "auto", parse: (e) => e },
  bv = [gi, V, Vt, yn, YC, XC, nE],
  Mh = (e) => bv.find(Nv(e)),
  cr = new Set();
let Ou = !1,
  ju = !1;
function Lv() {
  if (ju) {
    const e = Array.from(cr).filter((r) => r.needsMeasurement),
      t = new Set(e.map((r) => r.element)),
      n = new Map();
    t.forEach((r) => {
      const i = tE(r);
      i.length && (n.set(r, i), r.render());
    }),
      e.forEach((r) => r.measureInitialState()),
      t.forEach((r) => {
        r.render();
        const i = n.get(r);
        i &&
          i.forEach(([s, o]) => {
            var a;
            (a = r.getValue(s)) === null || a === void 0 || a.set(o);
          });
      }),
      e.forEach((r) => r.measureEndState()),
      e.forEach((r) => {
        r.suspendedScrollY !== void 0 && window.scrollTo(0, r.suspendedScrollY);
      });
  }
  (ju = !1), (Ou = !1), cr.forEach((e) => e.complete()), cr.clear();
}
function Ov() {
  cr.forEach((e) => {
    e.readKeyframes(), e.needsMeasurement && (ju = !0);
  });
}
function rE() {
  Ov(), Lv();
}
class ld {
  constructor(t, n, r, i, s, o = !1) {
    (this.isComplete = !1),
      (this.isAsync = !1),
      (this.needsMeasurement = !1),
      (this.isScheduled = !1),
      (this.unresolvedKeyframes = [...t]),
      (this.onComplete = n),
      (this.name = r),
      (this.motionValue = i),
      (this.element = s),
      (this.isAsync = o);
  }
  scheduleResolve() {
    (this.isScheduled = !0),
      this.isAsync
        ? (cr.add(this), Ou || ((Ou = !0), Y.read(Ov), Y.resolveKeyframes(Lv)))
        : (this.readKeyframes(), this.complete());
  }
  readKeyframes() {
    const {
      unresolvedKeyframes: t,
      name: n,
      element: r,
      motionValue: i,
    } = this;
    for (let s = 0; s < t.length; s++)
      if (t[s] === null)
        if (s === 0) {
          const o = i == null ? void 0 : i.get(),
            a = t[t.length - 1];
          if (o !== void 0) t[0] = o;
          else if (r && n) {
            const l = r.readValue(n, a);
            l != null && (t[0] = l);
          }
          t[0] === void 0 && (t[0] = a), i && o === void 0 && i.set(t[0]);
        } else t[s] = t[s - 1];
  }
  setFinalKeyframe() {}
  measureInitialState() {}
  renderEndStyles() {}
  measureEndState() {}
  complete() {
    (this.isComplete = !0),
      this.onComplete(this.unresolvedKeyframes, this.finalKeyframe),
      cr.delete(this);
  }
  cancel() {
    this.isComplete || ((this.isScheduled = !1), cr.delete(this));
  }
  resume() {
    this.isComplete || this.scheduleResolve();
  }
}
const Ki = (e) => Math.round(e * 1e5) / 1e5,
  ud = /-?(?:\d+(?:\.\d+)?|\.\d+)/gu;
function iE(e) {
  return e == null;
}
const sE =
    /^(?:#[\da-f]{3,8}|(?:rgb|hsl)a?\((?:-?[\d.]+%?[,\s]+){2}-?[\d.]+%?\s*(?:[,/]\s*)?(?:\b\d+(?:\.\d+)?|\.\d+)?%?\))$/iu,
  cd = (e, t) => (n) =>
    !!(
      (typeof n == "string" && sE.test(n) && n.startsWith(e)) ||
      (t && !iE(n) && Object.prototype.hasOwnProperty.call(n, t))
    ),
  jv = (e, t, n) => (r) => {
    if (typeof r != "string") return r;
    const [i, s, o, a] = r.match(ud);
    return {
      [e]: parseFloat(i),
      [t]: parseFloat(s),
      [n]: parseFloat(o),
      alpha: a !== void 0 ? parseFloat(a) : 1,
    };
  },
  oE = (e) => an(0, 255, e),
  Sl = { ...gi, transform: (e) => Math.round(oE(e)) },
  rr = {
    test: cd("rgb", "red"),
    parse: jv("red", "green", "blue"),
    transform: ({ red: e, green: t, blue: n, alpha: r = 1 }) =>
      "rgba(" +
      Sl.transform(e) +
      ", " +
      Sl.transform(t) +
      ", " +
      Sl.transform(n) +
      ", " +
      Ki(ys.transform(r)) +
      ")",
  };
function aE(e) {
  let t = "",
    n = "",
    r = "",
    i = "";
  return (
    e.length > 5
      ? ((t = e.substring(1, 3)),
        (n = e.substring(3, 5)),
        (r = e.substring(5, 7)),
        (i = e.substring(7, 9)))
      : ((t = e.substring(1, 2)),
        (n = e.substring(2, 3)),
        (r = e.substring(3, 4)),
        (i = e.substring(4, 5)),
        (t += t),
        (n += n),
        (r += r),
        (i += i)),
    {
      red: parseInt(t, 16),
      green: parseInt(n, 16),
      blue: parseInt(r, 16),
      alpha: i ? parseInt(i, 16) / 255 : 1,
    }
  );
}
const Iu = { test: cd("#"), parse: aE, transform: rr.transform },
  Or = {
    test: cd("hsl", "hue"),
    parse: jv("hue", "saturation", "lightness"),
    transform: ({ hue: e, saturation: t, lightness: n, alpha: r = 1 }) =>
      "hsla(" +
      Math.round(e) +
      ", " +
      Vt.transform(Ki(t)) +
      ", " +
      Vt.transform(Ki(n)) +
      ", " +
      Ki(ys.transform(r)) +
      ")",
  },
  Le = {
    test: (e) => rr.test(e) || Iu.test(e) || Or.test(e),
    parse: (e) =>
      rr.test(e) ? rr.parse(e) : Or.test(e) ? Or.parse(e) : Iu.parse(e),
    transform: (e) =>
      typeof e == "string"
        ? e
        : e.hasOwnProperty("red")
        ? rr.transform(e)
        : Or.transform(e),
  },
  lE =
    /(?:#[\da-f]{3,8}|(?:rgb|hsl)a?\((?:-?[\d.]+%?[,\s]+){2}-?[\d.]+%?\s*(?:[,/]\s*)?(?:\b\d+(?:\.\d+)?|\.\d+)?%?\))/giu;
function uE(e) {
  var t, n;
  return (
    isNaN(e) &&
    typeof e == "string" &&
    (((t = e.match(ud)) === null || t === void 0 ? void 0 : t.length) || 0) +
      (((n = e.match(lE)) === null || n === void 0 ? void 0 : n.length) || 0) >
      0
  );
}
const Iv = "number",
  Fv = "color",
  cE = "var",
  dE = "var(",
  Dh = "${}",
  fE =
    /var\s*\(\s*--(?:[\w-]+\s*|[\w-]+\s*,(?:\s*[^)(\s]|\s*\((?:[^)(]|\([^)(]*\))*\))+\s*)\)|#[\da-f]{3,8}|(?:rgb|hsl)a?\((?:-?[\d.]+%?[,\s]+){2}-?[\d.]+%?\s*(?:[,/]\s*)?(?:\b\d+(?:\.\d+)?|\.\d+)?%?\)|-?(?:\d+(?:\.\d+)?|\.\d+)/giu;
function vs(e) {
  const t = e.toString(),
    n = [],
    r = { color: [], number: [], var: [] },
    i = [];
  let s = 0;
  const a = t
    .replace(
      fE,
      (l) => (
        Le.test(l)
          ? (r.color.push(s), i.push(Fv), n.push(Le.parse(l)))
          : l.startsWith(dE)
          ? (r.var.push(s), i.push(cE), n.push(l))
          : (r.number.push(s), i.push(Iv), n.push(parseFloat(l))),
        ++s,
        Dh
      )
    )
    .split(Dh);
  return { values: n, split: a, indexes: r, types: i };
}
function _v(e) {
  return vs(e).values;
}
function Vv(e) {
  const { split: t, types: n } = vs(e),
    r = t.length;
  return (i) => {
    let s = "";
    for (let o = 0; o < r; o++)
      if (((s += t[o]), i[o] !== void 0)) {
        const a = n[o];
        a === Iv
          ? (s += Ki(i[o]))
          : a === Fv
          ? (s += Le.transform(i[o]))
          : (s += i[o]);
      }
    return s;
  };
}
const hE = (e) => (typeof e == "number" ? 0 : e);
function pE(e) {
  const t = _v(e);
  return Vv(e)(t.map(hE));
}
const Un = {
    test: uE,
    parse: _v,
    createTransformer: Vv,
    getAnimatableNone: pE,
  },
  mE = new Set(["brightness", "contrast", "saturate", "opacity"]);
function gE(e) {
  const [t, n] = e.slice(0, -1).split("(");
  if (t === "drop-shadow") return e;
  const [r] = n.match(ud) || [];
  if (!r) return e;
  const i = n.replace(r, "");
  let s = mE.has(t) ? 1 : 0;
  return r !== n && (s *= 100), t + "(" + s + i + ")";
}
const yE = /\b([a-z-]*)\(.*?\)/gu,
  Fu = {
    ...Un,
    getAnimatableNone: (e) => {
      const t = e.match(yE);
      return t ? t.map(gE).join(" ") : e;
    },
  },
  vE = {
    borderWidth: V,
    borderTopWidth: V,
    borderRightWidth: V,
    borderBottomWidth: V,
    borderLeftWidth: V,
    borderRadius: V,
    radius: V,
    borderTopLeftRadius: V,
    borderTopRightRadius: V,
    borderBottomRightRadius: V,
    borderBottomLeftRadius: V,
    width: V,
    maxWidth: V,
    height: V,
    maxHeight: V,
    top: V,
    right: V,
    bottom: V,
    left: V,
    padding: V,
    paddingTop: V,
    paddingRight: V,
    paddingBottom: V,
    paddingLeft: V,
    margin: V,
    marginTop: V,
    marginRight: V,
    marginBottom: V,
    marginLeft: V,
    backgroundPositionX: V,
    backgroundPositionY: V,
  },
  xE = {
    rotate: yn,
    rotateX: yn,
    rotateY: yn,
    rotateZ: yn,
    scale: io,
    scaleX: io,
    scaleY: io,
    scaleZ: io,
    skew: yn,
    skewX: yn,
    skewY: yn,
    distance: V,
    translateX: V,
    translateY: V,
    translateZ: V,
    x: V,
    y: V,
    z: V,
    perspective: V,
    transformPerspective: V,
    opacity: ys,
    originX: Th,
    originY: Th,
    originZ: V,
  },
  Nh = { ...gi, transform: Math.round },
  dd = {
    ...vE,
    ...xE,
    zIndex: Nh,
    size: V,
    fillOpacity: ys,
    strokeOpacity: ys,
    numOctaves: Nh,
  },
  wE = {
    ...dd,
    color: Le,
    backgroundColor: Le,
    outlineColor: Le,
    fill: Le,
    stroke: Le,
    borderColor: Le,
    borderTopColor: Le,
    borderRightColor: Le,
    borderBottomColor: Le,
    borderLeftColor: Le,
    filter: Fu,
    WebkitFilter: Fu,
  },
  fd = (e) => wE[e];
function zv(e, t) {
  let n = fd(e);
  return (
    n !== Fu && (n = Un), n.getAnimatableNone ? n.getAnimatableNone(t) : void 0
  );
}
const SE = new Set(["auto", "none", "0"]);
function PE(e, t, n) {
  let r = 0,
    i;
  for (; r < e.length && !i; ) {
    const s = e[r];
    typeof s == "string" && !SE.has(s) && vs(s).values.length && (i = e[r]),
      r++;
  }
  if (i && n) for (const s of t) e[s] = zv(n, i);
}
class Bv extends ld {
  constructor(t, n, r, i, s) {
    super(t, n, r, i, s, !0);
  }
  readKeyframes() {
    const { unresolvedKeyframes: t, element: n, name: r } = this;
    if (!n || !n.current) return;
    super.readKeyframes();
    for (let l = 0; l < t.length; l++) {
      let u = t[l];
      if (typeof u == "string" && ((u = u.trim()), ad(u))) {
        const c = Dv(u, n.current);
        c !== void 0 && (t[l] = c),
          l === t.length - 1 && (this.finalKeyframe = u);
      }
    }
    if ((this.resolveNoneKeyframes(), !ZC.has(r) || t.length !== 2)) return;
    const [i, s] = t,
      o = Mh(i),
      a = Mh(s);
    if (o !== a)
      if (kh(o) && kh(a))
        for (let l = 0; l < t.length; l++) {
          const u = t[l];
          typeof u == "string" && (t[l] = parseFloat(u));
        }
      else this.needsMeasurement = !0;
  }
  resolveNoneKeyframes() {
    const { unresolvedKeyframes: t, name: n } = this,
      r = [];
    for (let i = 0; i < t.length; i++) HC(t[i]) && r.push(i);
    r.length && PE(t, r, n);
  }
  measureInitialState() {
    const { element: t, unresolvedKeyframes: n, name: r } = this;
    if (!t || !t.current) return;
    r === "height" && (this.suspendedScrollY = window.pageYOffset),
      (this.measuredOrigin = ui[r](
        t.measureViewportBox(),
        window.getComputedStyle(t.current)
      )),
      (n[0] = this.measuredOrigin);
    const i = n[n.length - 1];
    i !== void 0 && t.getValue(r, i).jump(i, !1);
  }
  measureEndState() {
    var t;
    const { element: n, name: r, unresolvedKeyframes: i } = this;
    if (!n || !n.current) return;
    const s = n.getValue(r);
    s && s.jump(this.measuredOrigin, !1);
    const o = i.length - 1,
      a = i[o];
    (i[o] = ui[r](n.measureViewportBox(), window.getComputedStyle(n.current))),
      a !== null && this.finalKeyframe === void 0 && (this.finalKeyframe = a),
      !((t = this.removedTransforms) === null || t === void 0) &&
        t.length &&
        this.removedTransforms.forEach(([l, u]) => {
          n.getValue(l).set(u);
        }),
      this.resolveNoneKeyframes();
  }
}
function hd(e) {
  return typeof e == "function";
}
let So;
function CE() {
  So = void 0;
}
const zt = {
    now: () => (
      So === void 0 &&
        zt.set(
          ke.isProcessing || _C.useManualTiming
            ? ke.timestamp
            : performance.now()
        ),
      So
    ),
    set: (e) => {
      (So = e), queueMicrotask(CE);
    },
  },
  bh = (e, t) =>
    t === "zIndex"
      ? !1
      : !!(
          typeof e == "number" ||
          Array.isArray(e) ||
          (typeof e == "string" &&
            (Un.test(e) || e === "0") &&
            !e.startsWith("url("))
        );
function EE(e) {
  const t = e[0];
  if (e.length === 1) return !0;
  for (let n = 0; n < e.length; n++) if (e[n] !== t) return !0;
}
function TE(e, t, n, r) {
  const i = e[0];
  if (i === null) return !1;
  if (t === "display" || t === "visibility") return !0;
  const s = e[e.length - 1],
    o = bh(i, t),
    a = bh(s, t);
  return !o || !a ? !1 : EE(e) || ((n === "spring" || hd(n)) && r);
}
const kE = 40;
class Uv {
  constructor({
    autoplay: t = !0,
    delay: n = 0,
    type: r = "keyframes",
    repeat: i = 0,
    repeatDelay: s = 0,
    repeatType: o = "loop",
    ...a
  }) {
    (this.isStopped = !1),
      (this.hasAttemptedResolve = !1),
      (this.createdAt = zt.now()),
      (this.options = {
        autoplay: t,
        delay: n,
        type: r,
        repeat: i,
        repeatDelay: s,
        repeatType: o,
        ...a,
      }),
      this.updateFinishedPromise();
  }
  calcStartTime() {
    return this.resolvedAt
      ? this.resolvedAt - this.createdAt > kE
        ? this.resolvedAt
        : this.createdAt
      : this.createdAt;
  }
  get resolved() {
    return !this._resolved && !this.hasAttemptedResolve && rE(), this._resolved;
  }
  onKeyframesResolved(t, n) {
    (this.resolvedAt = zt.now()), (this.hasAttemptedResolve = !0);
    const {
      name: r,
      type: i,
      velocity: s,
      delay: o,
      onComplete: a,
      onUpdate: l,
      isGenerator: u,
    } = this.options;
    if (!u && !TE(t, r, i, s))
      if (o) this.options.duration = 0;
      else {
        l == null || l(Na(t, this.options, n)),
          a == null || a(),
          this.resolveFinishedPromise();
        return;
      }
    const c = this.initPlayback(t, n);
    c !== !1 &&
      ((this._resolved = { keyframes: t, finalKeyframe: n, ...c }),
      this.onPostResolved());
  }
  onPostResolved() {}
  then(t, n) {
    return this.currentFinishedPromise.then(t, n);
  }
  flatten() {
    (this.options.type = "keyframes"), (this.options.ease = "linear");
  }
  updateFinishedPromise() {
    this.currentFinishedPromise = new Promise((t) => {
      this.resolveFinishedPromise = t;
    });
  }
}
const ci = (e, t, n) => {
    const r = t - e;
    return r === 0 ? 1 : (n - e) / r;
  },
  $v = (e, t, n = 10) => {
    let r = "";
    const i = Math.max(Math.round(t / n), 2);
    for (let s = 0; s < i; s++) r += e(ci(0, i - 1, s)) + ", ";
    return `linear(${r.substring(0, r.length - 2)})`;
  };
function Wv(e, t) {
  return t ? e * (1e3 / t) : 0;
}
const AE = 5;
function Hv(e, t, n) {
  const r = Math.max(t - AE, 0);
  return Wv(n - e(r), t - r);
}
const fe = {
    stiffness: 100,
    damping: 10,
    mass: 1,
    velocity: 0,
    duration: 800,
    bounce: 0.3,
    visualDuration: 0.3,
    restSpeed: { granular: 0.01, default: 2 },
    restDelta: { granular: 0.005, default: 0.5 },
    minDuration: 0.01,
    maxDuration: 10,
    minDamping: 0.05,
    maxDamping: 1,
  },
  Pl = 0.001;
function RE({
  duration: e = fe.duration,
  bounce: t = fe.bounce,
  velocity: n = fe.velocity,
  mass: r = fe.mass,
}) {
  let i,
    s,
    o = 1 - t;
  (o = an(fe.minDamping, fe.maxDamping, o)),
    (e = an(fe.minDuration, fe.maxDuration, en(e))),
    o < 1
      ? ((i = (u) => {
          const c = u * o,
            d = c * e,
            f = c - n,
            v = _u(u, o),
            y = Math.exp(-d);
          return Pl - (f / v) * y;
        }),
        (s = (u) => {
          const d = u * o * e,
            f = d * n + n,
            v = Math.pow(o, 2) * Math.pow(u, 2) * e,
            y = Math.exp(-d),
            m = _u(Math.pow(u, 2), o);
          return ((-i(u) + Pl > 0 ? -1 : 1) * ((f - v) * y)) / m;
        }))
      : ((i = (u) => {
          const c = Math.exp(-u * e),
            d = (u - n) * e + 1;
          return -Pl + c * d;
        }),
        (s = (u) => {
          const c = Math.exp(-u * e),
            d = (n - u) * (e * e);
          return c * d;
        }));
  const a = 5 / e,
    l = DE(i, s, a);
  if (((e = Jt(e)), isNaN(l)))
    return { stiffness: fe.stiffness, damping: fe.damping, duration: e };
  {
    const u = Math.pow(l, 2) * r;
    return { stiffness: u, damping: o * 2 * Math.sqrt(r * u), duration: e };
  }
}
const ME = 12;
function DE(e, t, n) {
  let r = n;
  for (let i = 1; i < ME; i++) r = r - e(r) / t(r);
  return r;
}
function _u(e, t) {
  return e * Math.sqrt(1 - t * t);
}
const Vu = 2e4;
function Kv(e) {
  let t = 0;
  const n = 50;
  let r = e.next(t);
  for (; !r.done && t < Vu; ) (t += n), (r = e.next(t));
  return t >= Vu ? 1 / 0 : t;
}
const NE = ["duration", "bounce"],
  bE = ["stiffness", "damping", "mass"];
function Lh(e, t) {
  return t.some((n) => e[n] !== void 0);
}
function LE(e) {
  let t = {
    velocity: fe.velocity,
    stiffness: fe.stiffness,
    damping: fe.damping,
    mass: fe.mass,
    isResolvedFromDuration: !1,
    ...e,
  };
  if (!Lh(e, bE) && Lh(e, NE))
    if (e.visualDuration) {
      const n = e.visualDuration,
        r = (2 * Math.PI) / (n * 1.2),
        i = r * r,
        s = 2 * an(0.05, 1, 1 - e.bounce) * Math.sqrt(i);
      t = { ...t, mass: fe.mass, stiffness: i, damping: s };
    } else {
      const n = RE(e);
      (t = { ...t, ...n, mass: fe.mass }), (t.isResolvedFromDuration = !0);
    }
  return t;
}
function Qv(e = fe.visualDuration, t = fe.bounce) {
  const n =
    typeof e != "object"
      ? { visualDuration: e, keyframes: [0, 1], bounce: t }
      : e;
  let { restSpeed: r, restDelta: i } = n;
  const s = n.keyframes[0],
    o = n.keyframes[n.keyframes.length - 1],
    a = { done: !1, value: s },
    {
      stiffness: l,
      damping: u,
      mass: c,
      duration: d,
      velocity: f,
      isResolvedFromDuration: v,
    } = LE({ ...n, velocity: -en(n.velocity || 0) }),
    y = f || 0,
    m = u / (2 * Math.sqrt(l * c)),
    x = o - s,
    h = en(Math.sqrt(l / c)),
    p = Math.abs(x) < 5;
  r || (r = p ? fe.restSpeed.granular : fe.restSpeed.default),
    i || (i = p ? fe.restDelta.granular : fe.restDelta.default);
  let g;
  if (m < 1) {
    const C = _u(h, m);
    g = (k) => {
      const T = Math.exp(-m * h * k);
      return (
        o - T * (((y + m * h * x) / C) * Math.sin(C * k) + x * Math.cos(C * k))
      );
    };
  } else if (m === 1) g = (C) => o - Math.exp(-h * C) * (x + (y + h * x) * C);
  else {
    const C = h * Math.sqrt(m * m - 1);
    g = (k) => {
      const T = Math.exp(-m * h * k),
        E = Math.min(C * k, 300);
      return (
        o - (T * ((y + m * h * x) * Math.sinh(E) + C * x * Math.cosh(E))) / C
      );
    };
  }
  const S = {
    calculatedDuration: (v && d) || null,
    next: (C) => {
      const k = g(C);
      if (v) a.done = C >= d;
      else {
        let T = 0;
        m < 1 && (T = C === 0 ? Jt(y) : Hv(g, C, k));
        const E = Math.abs(T) <= r,
          D = Math.abs(o - k) <= i;
        a.done = E && D;
      }
      return (a.value = a.done ? o : k), a;
    },
    toString: () => {
      const C = Math.min(Kv(S), Vu),
        k = $v((T) => S.next(C * T).value, C, 30);
      return C + "ms " + k;
    },
  };
  return S;
}
function Oh({
  keyframes: e,
  velocity: t = 0,
  power: n = 0.8,
  timeConstant: r = 325,
  bounceDamping: i = 10,
  bounceStiffness: s = 500,
  modifyTarget: o,
  min: a,
  max: l,
  restDelta: u = 0.5,
  restSpeed: c,
}) {
  const d = e[0],
    f = { done: !1, value: d },
    v = (E) => (a !== void 0 && E < a) || (l !== void 0 && E > l),
    y = (E) =>
      a === void 0
        ? l
        : l === void 0 || Math.abs(a - E) < Math.abs(l - E)
        ? a
        : l;
  let m = n * t;
  const x = d + m,
    h = o === void 0 ? x : o(x);
  h !== x && (m = h - d);
  const p = (E) => -m * Math.exp(-E / r),
    g = (E) => h + p(E),
    S = (E) => {
      const D = p(E),
        N = g(E);
      (f.done = Math.abs(D) <= u), (f.value = f.done ? h : N);
    };
  let C, k;
  const T = (E) => {
    v(f.value) &&
      ((C = E),
      (k = Qv({
        keyframes: [f.value, y(f.value)],
        velocity: Hv(g, E, f.value),
        damping: i,
        stiffness: s,
        restDelta: u,
        restSpeed: c,
      })));
  };
  return (
    T(0),
    {
      calculatedDuration: null,
      next: (E) => {
        let D = !1;
        return (
          !k && C === void 0 && ((D = !0), S(E), T(E)),
          C !== void 0 && E >= C ? k.next(E - C) : (!D && S(E), f)
        );
      },
    }
  );
}
const OE = Ns(0.42, 0, 1, 1),
  jE = Ns(0, 0, 0.58, 1),
  Gv = Ns(0.42, 0, 0.58, 1),
  IE = (e) => Array.isArray(e) && typeof e[0] != "number",
  pd = (e) => Array.isArray(e) && typeof e[0] == "number",
  jh = {
    linear: Ie,
    easeIn: OE,
    easeInOut: Gv,
    easeOut: jE,
    circIn: od,
    circInOut: Tv,
    circOut: Ev,
    backIn: sd,
    backInOut: Pv,
    backOut: Sv,
    anticipate: Cv,
  },
  Ih = (e) => {
    if (pd(e)) {
      Lu(e.length === 4);
      const [t, n, r, i] = e;
      return Ns(t, n, r, i);
    } else if (typeof e == "string") return Lu(jh[e] !== void 0), jh[e];
    return e;
  },
  FE = (e, t) => (n) => t(e(n)),
  Fn = (...e) => e.reduce(FE),
  ae = (e, t, n) => e + (t - e) * n;
function Cl(e, t, n) {
  return (
    n < 0 && (n += 1),
    n > 1 && (n -= 1),
    n < 1 / 6
      ? e + (t - e) * 6 * n
      : n < 1 / 2
      ? t
      : n < 2 / 3
      ? e + (t - e) * (2 / 3 - n) * 6
      : e
  );
}
function _E({ hue: e, saturation: t, lightness: n, alpha: r }) {
  (e /= 360), (t /= 100), (n /= 100);
  let i = 0,
    s = 0,
    o = 0;
  if (!t) i = s = o = n;
  else {
    const a = n < 0.5 ? n * (1 + t) : n + t - n * t,
      l = 2 * n - a;
    (i = Cl(l, a, e + 1 / 3)), (s = Cl(l, a, e)), (o = Cl(l, a, e - 1 / 3));
  }
  return {
    red: Math.round(i * 255),
    green: Math.round(s * 255),
    blue: Math.round(o * 255),
    alpha: r,
  };
}
function Xo(e, t) {
  return (n) => (n > 0 ? t : e);
}
const El = (e, t, n) => {
    const r = e * e,
      i = n * (t * t - r) + r;
    return i < 0 ? 0 : Math.sqrt(i);
  },
  VE = [Iu, rr, Or],
  zE = (e) => VE.find((t) => t.test(e));
function Fh(e) {
  const t = zE(e);
  if (!t) return !1;
  let n = t.parse(e);
  return t === Or && (n = _E(n)), n;
}
const _h = (e, t) => {
    const n = Fh(e),
      r = Fh(t);
    if (!n || !r) return Xo(e, t);
    const i = { ...n };
    return (s) => (
      (i.red = El(n.red, r.red, s)),
      (i.green = El(n.green, r.green, s)),
      (i.blue = El(n.blue, r.blue, s)),
      (i.alpha = ae(n.alpha, r.alpha, s)),
      rr.transform(i)
    );
  },
  zu = new Set(["none", "hidden"]);
function BE(e, t) {
  return zu.has(e) ? (n) => (n <= 0 ? e : t) : (n) => (n >= 1 ? t : e);
}
function UE(e, t) {
  return (n) => ae(e, t, n);
}
function md(e) {
  return typeof e == "number"
    ? UE
    : typeof e == "string"
    ? ad(e)
      ? Xo
      : Le.test(e)
      ? _h
      : HE
    : Array.isArray(e)
    ? qv
    : typeof e == "object"
    ? Le.test(e)
      ? _h
      : $E
    : Xo;
}
function qv(e, t) {
  const n = [...e],
    r = n.length,
    i = e.map((s, o) => md(s)(s, t[o]));
  return (s) => {
    for (let o = 0; o < r; o++) n[o] = i[o](s);
    return n;
  };
}
function $E(e, t) {
  const n = { ...e, ...t },
    r = {};
  for (const i in n)
    e[i] !== void 0 && t[i] !== void 0 && (r[i] = md(e[i])(e[i], t[i]));
  return (i) => {
    for (const s in r) n[s] = r[s](i);
    return n;
  };
}
function WE(e, t) {
  var n;
  const r = [],
    i = { color: 0, var: 0, number: 0 };
  for (let s = 0; s < t.values.length; s++) {
    const o = t.types[s],
      a = e.indexes[o][i[o]],
      l = (n = e.values[a]) !== null && n !== void 0 ? n : 0;
    (r[s] = l), i[o]++;
  }
  return r;
}
const HE = (e, t) => {
  const n = Un.createTransformer(t),
    r = vs(e),
    i = vs(t);
  return r.indexes.var.length === i.indexes.var.length &&
    r.indexes.color.length === i.indexes.color.length &&
    r.indexes.number.length >= i.indexes.number.length
    ? (zu.has(e) && !i.values.length) || (zu.has(t) && !r.values.length)
      ? BE(e, t)
      : Fn(qv(WE(r, i), i.values), n)
    : Xo(e, t);
};
function Xv(e, t, n) {
  return typeof e == "number" && typeof t == "number" && typeof n == "number"
    ? ae(e, t, n)
    : md(e)(e, t);
}
function KE(e, t, n) {
  const r = [],
    i = n || Xv,
    s = e.length - 1;
  for (let o = 0; o < s; o++) {
    let a = i(e[o], e[o + 1]);
    if (t) {
      const l = Array.isArray(t) ? t[o] || Ie : t;
      a = Fn(l, a);
    }
    r.push(a);
  }
  return r;
}
function QE(e, t, { clamp: n = !0, ease: r, mixer: i } = {}) {
  const s = e.length;
  if ((Lu(s === t.length), s === 1)) return () => t[0];
  if (s === 2 && e[0] === e[1]) return () => t[1];
  e[0] > e[s - 1] && ((e = [...e].reverse()), (t = [...t].reverse()));
  const o = KE(t, r, i),
    a = o.length,
    l = (u) => {
      let c = 0;
      if (a > 1) for (; c < e.length - 2 && !(u < e[c + 1]); c++);
      const d = ci(e[c], e[c + 1], u);
      return o[c](d);
    };
  return n ? (u) => l(an(e[0], e[s - 1], u)) : l;
}
function GE(e, t) {
  const n = e[e.length - 1];
  for (let r = 1; r <= t; r++) {
    const i = ci(0, t, r);
    e.push(ae(n, 1, i));
  }
}
function qE(e) {
  const t = [0];
  return GE(t, e.length - 1), t;
}
function XE(e, t) {
  return e.map((n) => n * t);
}
function YE(e, t) {
  return e.map(() => t || Gv).splice(0, e.length - 1);
}
function Yo({
  duration: e = 300,
  keyframes: t,
  times: n,
  ease: r = "easeInOut",
}) {
  const i = IE(r) ? r.map(Ih) : Ih(r),
    s = { done: !1, value: t[0] },
    o = XE(n && n.length === t.length ? n : qE(t), e),
    a = QE(o, t, { ease: Array.isArray(i) ? i : YE(t, i) });
  return {
    calculatedDuration: e,
    next: (l) => ((s.value = a(l)), (s.done = l >= e), s),
  };
}
const ZE = (e) => {
    const t = ({ timestamp: n }) => e(n);
    return {
      start: () => Y.update(t, !0),
      stop: () => Bn(t),
      now: () => (ke.isProcessing ? ke.timestamp : zt.now()),
    };
  },
  JE = { decay: Oh, inertia: Oh, tween: Yo, keyframes: Yo, spring: Qv },
  eT = (e) => e / 100;
class gd extends Uv {
  constructor(t) {
    super(t),
      (this.holdTime = null),
      (this.cancelTime = null),
      (this.currentTime = 0),
      (this.playbackSpeed = 1),
      (this.pendingPlayState = "running"),
      (this.startTime = null),
      (this.state = "idle"),
      (this.stop = () => {
        if (
          (this.resolver.cancel(), (this.isStopped = !0), this.state === "idle")
        )
          return;
        this.teardown();
        const { onStop: l } = this.options;
        l && l();
      });
    const { name: n, motionValue: r, element: i, keyframes: s } = this.options,
      o = (i == null ? void 0 : i.KeyframeResolver) || ld,
      a = (l, u) => this.onKeyframesResolved(l, u);
    (this.resolver = new o(s, a, n, r, i)), this.resolver.scheduleResolve();
  }
  flatten() {
    super.flatten(),
      this._resolved &&
        Object.assign(
          this._resolved,
          this.initPlayback(this._resolved.keyframes)
        );
  }
  initPlayback(t) {
    const {
        type: n = "keyframes",
        repeat: r = 0,
        repeatDelay: i = 0,
        repeatType: s,
        velocity: o = 0,
      } = this.options,
      a = hd(n) ? n : JE[n] || Yo;
    let l, u;
    a !== Yo &&
      typeof t[0] != "number" &&
      ((l = Fn(eT, Xv(t[0], t[1]))), (t = [0, 100]));
    const c = a({ ...this.options, keyframes: t });
    s === "mirror" &&
      (u = a({ ...this.options, keyframes: [...t].reverse(), velocity: -o })),
      c.calculatedDuration === null && (c.calculatedDuration = Kv(c));
    const { calculatedDuration: d } = c,
      f = d + i,
      v = f * (r + 1) - i;
    return {
      generator: c,
      mirroredGenerator: u,
      mapPercentToKeyframes: l,
      calculatedDuration: d,
      resolvedDuration: f,
      totalDuration: v,
    };
  }
  onPostResolved() {
    const { autoplay: t = !0 } = this.options;
    this.play(),
      this.pendingPlayState === "paused" || !t
        ? this.pause()
        : (this.state = this.pendingPlayState);
  }
  tick(t, n = !1) {
    const { resolved: r } = this;
    if (!r) {
      const { keyframes: E } = this.options;
      return { done: !0, value: E[E.length - 1] };
    }
    const {
      finalKeyframe: i,
      generator: s,
      mirroredGenerator: o,
      mapPercentToKeyframes: a,
      keyframes: l,
      calculatedDuration: u,
      totalDuration: c,
      resolvedDuration: d,
    } = r;
    if (this.startTime === null) return s.next(0);
    const {
      delay: f,
      repeat: v,
      repeatType: y,
      repeatDelay: m,
      onUpdate: x,
    } = this.options;
    this.speed > 0
      ? (this.startTime = Math.min(this.startTime, t))
      : this.speed < 0 &&
        (this.startTime = Math.min(t - c / this.speed, this.startTime)),
      n
        ? (this.currentTime = t)
        : this.holdTime !== null
        ? (this.currentTime = this.holdTime)
        : (this.currentTime = Math.round(t - this.startTime) * this.speed);
    const h = this.currentTime - f * (this.speed >= 0 ? 1 : -1),
      p = this.speed >= 0 ? h < 0 : h > c;
    (this.currentTime = Math.max(h, 0)),
      this.state === "finished" &&
        this.holdTime === null &&
        (this.currentTime = c);
    let g = this.currentTime,
      S = s;
    if (v) {
      const E = Math.min(this.currentTime, c) / d;
      let D = Math.floor(E),
        N = E % 1;
      !N && E >= 1 && (N = 1),
        N === 1 && D--,
        (D = Math.min(D, v + 1)),
        !!(D % 2) &&
          (y === "reverse"
            ? ((N = 1 - N), m && (N -= m / d))
            : y === "mirror" && (S = o)),
        (g = an(0, 1, N) * d);
    }
    const C = p ? { done: !1, value: l[0] } : S.next(g);
    a && (C.value = a(C.value));
    let { done: k } = C;
    !p &&
      u !== null &&
      (k = this.speed >= 0 ? this.currentTime >= c : this.currentTime <= 0);
    const T =
      this.holdTime === null &&
      (this.state === "finished" || (this.state === "running" && k));
    return (
      T && i !== void 0 && (C.value = Na(l, this.options, i)),
      x && x(C.value),
      T && this.finish(),
      C
    );
  }
  get duration() {
    const { resolved: t } = this;
    return t ? en(t.calculatedDuration) : 0;
  }
  get time() {
    return en(this.currentTime);
  }
  set time(t) {
    (t = Jt(t)),
      (this.currentTime = t),
      this.holdTime !== null || this.speed === 0
        ? (this.holdTime = t)
        : this.driver && (this.startTime = this.driver.now() - t / this.speed);
  }
  get speed() {
    return this.playbackSpeed;
  }
  set speed(t) {
    const n = this.playbackSpeed !== t;
    (this.playbackSpeed = t), n && (this.time = en(this.currentTime));
  }
  play() {
    if (
      (this.resolver.isScheduled || this.resolver.resume(), !this._resolved)
    ) {
      this.pendingPlayState = "running";
      return;
    }
    if (this.isStopped) return;
    const { driver: t = ZE, onPlay: n, startTime: r } = this.options;
    this.driver || (this.driver = t((s) => this.tick(s))), n && n();
    const i = this.driver.now();
    this.holdTime !== null
      ? (this.startTime = i - this.holdTime)
      : this.startTime
      ? this.state === "finished" && (this.startTime = i)
      : (this.startTime = r ?? this.calcStartTime()),
      this.state === "finished" && this.updateFinishedPromise(),
      (this.cancelTime = this.startTime),
      (this.holdTime = null),
      (this.state = "running"),
      this.driver.start();
  }
  pause() {
    var t;
    if (!this._resolved) {
      this.pendingPlayState = "paused";
      return;
    }
    (this.state = "paused"),
      (this.holdTime = (t = this.currentTime) !== null && t !== void 0 ? t : 0);
  }
  complete() {
    this.state !== "running" && this.play(),
      (this.pendingPlayState = this.state = "finished"),
      (this.holdTime = null);
  }
  finish() {
    this.teardown(), (this.state = "finished");
    const { onComplete: t } = this.options;
    t && t();
  }
  cancel() {
    this.cancelTime !== null && this.tick(this.cancelTime),
      this.teardown(),
      this.updateFinishedPromise();
  }
  teardown() {
    (this.state = "idle"),
      this.stopDriver(),
      this.resolveFinishedPromise(),
      this.updateFinishedPromise(),
      (this.startTime = this.cancelTime = null),
      this.resolver.cancel();
  }
  stopDriver() {
    this.driver && (this.driver.stop(), (this.driver = void 0));
  }
  sample(t) {
    return (this.startTime = 0), this.tick(t, !0);
  }
}
const tT = new Set(["opacity", "clipPath", "filter", "transform"]);
function yd(e) {
  let t;
  return () => (t === void 0 && (t = e()), t);
}
const nT = { linearEasing: void 0 };
function rT(e, t) {
  const n = yd(e);
  return () => {
    var r;
    return (r = nT[t]) !== null && r !== void 0 ? r : n();
  };
}
const Zo = rT(() => {
  try {
    document
      .createElement("div")
      .animate({ opacity: 0 }, { easing: "linear(0, 1)" });
  } catch {
    return !1;
  }
  return !0;
}, "linearEasing");
function Yv(e) {
  return !!(
    (typeof e == "function" && Zo()) ||
    !e ||
    (typeof e == "string" && (e in Bu || Zo())) ||
    pd(e) ||
    (Array.isArray(e) && e.every(Yv))
  );
}
const Li = ([e, t, n, r]) => `cubic-bezier(${e}, ${t}, ${n}, ${r})`,
  Bu = {
    linear: "linear",
    ease: "ease",
    easeIn: "ease-in",
    easeOut: "ease-out",
    easeInOut: "ease-in-out",
    circIn: Li([0, 0.65, 0.55, 1]),
    circOut: Li([0.55, 0, 1, 0.45]),
    backIn: Li([0.31, 0.01, 0.66, -0.59]),
    backOut: Li([0.33, 1.53, 0.69, 0.99]),
  };
function Zv(e, t) {
  if (e)
    return typeof e == "function" && Zo()
      ? $v(e, t)
      : pd(e)
      ? Li(e)
      : Array.isArray(e)
      ? e.map((n) => Zv(n, t) || Bu.easeOut)
      : Bu[e];
}
function iT(
  e,
  t,
  n,
  {
    delay: r = 0,
    duration: i = 300,
    repeat: s = 0,
    repeatType: o = "loop",
    ease: a = "easeInOut",
    times: l,
  } = {}
) {
  const u = { [t]: n };
  l && (u.offset = l);
  const c = Zv(a, i);
  return (
    Array.isArray(c) && (u.easing = c),
    e.animate(u, {
      delay: r,
      duration: i,
      easing: Array.isArray(c) ? "linear" : c,
      fill: "both",
      iterations: s + 1,
      direction: o === "reverse" ? "alternate" : "normal",
    })
  );
}
function Vh(e, t) {
  (e.timeline = t), (e.onfinish = null);
}
const sT = yd(() => Object.hasOwnProperty.call(Element.prototype, "animate")),
  Jo = 10,
  oT = 2e4;
function aT(e) {
  return hd(e.type) || e.type === "spring" || !Yv(e.ease);
}
function lT(e, t) {
  const n = new gd({
    ...t,
    keyframes: e,
    repeat: 0,
    delay: 0,
    isGenerator: !0,
  });
  let r = { done: !1, value: e[0] };
  const i = [];
  let s = 0;
  for (; !r.done && s < oT; ) (r = n.sample(s)), i.push(r.value), (s += Jo);
  return { times: void 0, keyframes: i, duration: s - Jo, ease: "linear" };
}
const Jv = { anticipate: Cv, backInOut: Pv, circInOut: Tv };
function uT(e) {
  return e in Jv;
}
class zh extends Uv {
  constructor(t) {
    super(t);
    const { name: n, motionValue: r, element: i, keyframes: s } = this.options;
    (this.resolver = new Bv(
      s,
      (o, a) => this.onKeyframesResolved(o, a),
      n,
      r,
      i
    )),
      this.resolver.scheduleResolve();
  }
  initPlayback(t, n) {
    var r;
    let {
      duration: i = 300,
      times: s,
      ease: o,
      type: a,
      motionValue: l,
      name: u,
      startTime: c,
    } = this.options;
    if (!(!((r = l.owner) === null || r === void 0) && r.current)) return !1;
    if (
      (typeof o == "string" && Zo() && uT(o) && (o = Jv[o]), aT(this.options))
    ) {
      const {
          onComplete: f,
          onUpdate: v,
          motionValue: y,
          element: m,
          ...x
        } = this.options,
        h = lT(t, x);
      (t = h.keyframes),
        t.length === 1 && (t[1] = t[0]),
        (i = h.duration),
        (s = h.times),
        (o = h.ease),
        (a = "keyframes");
    }
    const d = iT(l.owner.current, u, t, {
      ...this.options,
      duration: i,
      times: s,
      ease: o,
    });
    return (
      (d.startTime = c ?? this.calcStartTime()),
      this.pendingTimeline
        ? (Vh(d, this.pendingTimeline), (this.pendingTimeline = void 0))
        : (d.onfinish = () => {
            const { onComplete: f } = this.options;
            l.set(Na(t, this.options, n)),
              f && f(),
              this.cancel(),
              this.resolveFinishedPromise();
          }),
      { animation: d, duration: i, times: s, type: a, ease: o, keyframes: t }
    );
  }
  get duration() {
    const { resolved: t } = this;
    if (!t) return 0;
    const { duration: n } = t;
    return en(n);
  }
  get time() {
    const { resolved: t } = this;
    if (!t) return 0;
    const { animation: n } = t;
    return en(n.currentTime || 0);
  }
  set time(t) {
    const { resolved: n } = this;
    if (!n) return;
    const { animation: r } = n;
    r.currentTime = Jt(t);
  }
  get speed() {
    const { resolved: t } = this;
    if (!t) return 1;
    const { animation: n } = t;
    return n.playbackRate;
  }
  set speed(t) {
    const { resolved: n } = this;
    if (!n) return;
    const { animation: r } = n;
    r.playbackRate = t;
  }
  get state() {
    const { resolved: t } = this;
    if (!t) return "idle";
    const { animation: n } = t;
    return n.playState;
  }
  get startTime() {
    const { resolved: t } = this;
    if (!t) return null;
    const { animation: n } = t;
    return n.startTime;
  }
  attachTimeline(t) {
    if (!this._resolved) this.pendingTimeline = t;
    else {
      const { resolved: n } = this;
      if (!n) return Ie;
      const { animation: r } = n;
      Vh(r, t);
    }
    return Ie;
  }
  play() {
    if (this.isStopped) return;
    const { resolved: t } = this;
    if (!t) return;
    const { animation: n } = t;
    n.playState === "finished" && this.updateFinishedPromise(), n.play();
  }
  pause() {
    const { resolved: t } = this;
    if (!t) return;
    const { animation: n } = t;
    n.pause();
  }
  stop() {
    if ((this.resolver.cancel(), (this.isStopped = !0), this.state === "idle"))
      return;
    this.resolveFinishedPromise(), this.updateFinishedPromise();
    const { resolved: t } = this;
    if (!t) return;
    const {
      animation: n,
      keyframes: r,
      duration: i,
      type: s,
      ease: o,
      times: a,
    } = t;
    if (n.playState === "idle" || n.playState === "finished") return;
    if (this.time) {
      const {
          motionValue: u,
          onUpdate: c,
          onComplete: d,
          element: f,
          ...v
        } = this.options,
        y = new gd({
          ...v,
          keyframes: r,
          duration: i,
          type: s,
          ease: o,
          times: a,
          isGenerator: !0,
        }),
        m = Jt(this.time);
      u.setWithVelocity(y.sample(m - Jo).value, y.sample(m).value, Jo);
    }
    const { onStop: l } = this.options;
    l && l(), this.cancel();
  }
  complete() {
    const { resolved: t } = this;
    t && t.animation.finish();
  }
  cancel() {
    const { resolved: t } = this;
    t && t.animation.cancel();
  }
  static supports(t) {
    const {
      motionValue: n,
      name: r,
      repeatDelay: i,
      repeatType: s,
      damping: o,
      type: a,
    } = t;
    return (
      sT() &&
      r &&
      tT.has(r) &&
      n &&
      n.owner &&
      n.owner.current instanceof HTMLElement &&
      !n.owner.getProps().onUpdate &&
      !i &&
      s !== "mirror" &&
      o !== 0 &&
      a !== "inertia"
    );
  }
}
const cT = yd(() => window.ScrollTimeline !== void 0);
class dT {
  constructor(t) {
    (this.stop = () => this.runAll("stop")),
      (this.animations = t.filter(Boolean));
  }
  then(t, n) {
    return Promise.all(this.animations).then(t).catch(n);
  }
  getAll(t) {
    return this.animations[0][t];
  }
  setAll(t, n) {
    for (let r = 0; r < this.animations.length; r++) this.animations[r][t] = n;
  }
  attachTimeline(t, n) {
    const r = this.animations.map((i) =>
      cT() && i.attachTimeline ? i.attachTimeline(t) : n(i)
    );
    return () => {
      r.forEach((i, s) => {
        i && i(), this.animations[s].stop();
      });
    };
  }
  get time() {
    return this.getAll("time");
  }
  set time(t) {
    this.setAll("time", t);
  }
  get speed() {
    return this.getAll("speed");
  }
  set speed(t) {
    this.setAll("speed", t);
  }
  get startTime() {
    return this.getAll("startTime");
  }
  get duration() {
    let t = 0;
    for (let n = 0; n < this.animations.length; n++)
      t = Math.max(t, this.animations[n].duration);
    return t;
  }
  runAll(t) {
    this.animations.forEach((n) => n[t]());
  }
  flatten() {
    this.runAll("flatten");
  }
  play() {
    this.runAll("play");
  }
  pause() {
    this.runAll("pause");
  }
  cancel() {
    this.runAll("cancel");
  }
  complete() {
    this.runAll("complete");
  }
}
function fT({
  when: e,
  delay: t,
  delayChildren: n,
  staggerChildren: r,
  staggerDirection: i,
  repeat: s,
  repeatType: o,
  repeatDelay: a,
  from: l,
  elapsed: u,
  ...c
}) {
  return !!Object.keys(c).length;
}
const vd =
    (e, t, n, r = {}, i, s) =>
    (o) => {
      const a = id(r, e) || {},
        l = a.delay || r.delay || 0;
      let { elapsed: u = 0 } = r;
      u = u - Jt(l);
      let c = {
        keyframes: Array.isArray(n) ? n : [null, n],
        ease: "easeOut",
        velocity: t.getVelocity(),
        ...a,
        delay: -u,
        onUpdate: (f) => {
          t.set(f), a.onUpdate && a.onUpdate(f);
        },
        onComplete: () => {
          o(), a.onComplete && a.onComplete();
        },
        name: e,
        motionValue: t,
        element: s ? void 0 : i,
      };
      fT(a) || (c = { ...c, ...FC(e, c) }),
        c.duration && (c.duration = Jt(c.duration)),
        c.repeatDelay && (c.repeatDelay = Jt(c.repeatDelay)),
        c.from !== void 0 && (c.keyframes[0] = c.from);
      let d = !1;
      if (
        ((c.type === !1 || (c.duration === 0 && !c.repeatDelay)) &&
          ((c.duration = 0), c.delay === 0 && (d = !0)),
        d && !s && t.get() !== void 0)
      ) {
        const f = Na(c.keyframes, a);
        if (f !== void 0)
          return (
            Y.update(() => {
              c.onUpdate(f), c.onComplete();
            }),
            new dT([])
          );
      }
      return !s && zh.supports(c) ? new zh(c) : new gd(c);
    },
  hT = (e) => !!(e && typeof e == "object" && e.mix && e.toValue),
  pT = (e) => (bu(e) ? e[e.length - 1] || 0 : e);
function xd(e, t) {
  e.indexOf(t) === -1 && e.push(t);
}
function wd(e, t) {
  const n = e.indexOf(t);
  n > -1 && e.splice(n, 1);
}
class Sd {
  constructor() {
    this.subscriptions = [];
  }
  add(t) {
    return xd(this.subscriptions, t), () => wd(this.subscriptions, t);
  }
  notify(t, n, r) {
    const i = this.subscriptions.length;
    if (i)
      if (i === 1) this.subscriptions[0](t, n, r);
      else
        for (let s = 0; s < i; s++) {
          const o = this.subscriptions[s];
          o && o(t, n, r);
        }
  }
  getSize() {
    return this.subscriptions.length;
  }
  clear() {
    this.subscriptions.length = 0;
  }
}
const Bh = 30,
  mT = (e) => !isNaN(parseFloat(e));
class gT {
  constructor(t, n = {}) {
    (this.version = "11.13.1"),
      (this.canTrackVelocity = null),
      (this.events = {}),
      (this.updateAndNotify = (r, i = !0) => {
        const s = zt.now();
        this.updatedAt !== s && this.setPrevFrameValue(),
          (this.prev = this.current),
          this.setCurrent(r),
          this.current !== this.prev &&
            this.events.change &&
            this.events.change.notify(this.current),
          i &&
            this.events.renderRequest &&
            this.events.renderRequest.notify(this.current);
      }),
      (this.hasAnimated = !1),
      this.setCurrent(t),
      (this.owner = n.owner);
  }
  setCurrent(t) {
    (this.current = t),
      (this.updatedAt = zt.now()),
      this.canTrackVelocity === null &&
        t !== void 0 &&
        (this.canTrackVelocity = mT(this.current));
  }
  setPrevFrameValue(t = this.current) {
    (this.prevFrameValue = t), (this.prevUpdatedAt = this.updatedAt);
  }
  onChange(t) {
    return this.on("change", t);
  }
  on(t, n) {
    this.events[t] || (this.events[t] = new Sd());
    const r = this.events[t].add(n);
    return t === "change"
      ? () => {
          r(),
            Y.read(() => {
              this.events.change.getSize() || this.stop();
            });
        }
      : r;
  }
  clearListeners() {
    for (const t in this.events) this.events[t].clear();
  }
  attach(t, n) {
    (this.passiveEffect = t), (this.stopPassiveEffect = n);
  }
  set(t, n = !0) {
    !n || !this.passiveEffect
      ? this.updateAndNotify(t, n)
      : this.passiveEffect(t, this.updateAndNotify);
  }
  setWithVelocity(t, n, r) {
    this.set(n),
      (this.prev = void 0),
      (this.prevFrameValue = t),
      (this.prevUpdatedAt = this.updatedAt - r);
  }
  jump(t, n = !0) {
    this.updateAndNotify(t),
      (this.prev = t),
      (this.prevUpdatedAt = this.prevFrameValue = void 0),
      n && this.stop(),
      this.stopPassiveEffect && this.stopPassiveEffect();
  }
  get() {
    return this.current;
  }
  getPrevious() {
    return this.prev;
  }
  getVelocity() {
    const t = zt.now();
    if (
      !this.canTrackVelocity ||
      this.prevFrameValue === void 0 ||
      t - this.updatedAt > Bh
    )
      return 0;
    const n = Math.min(this.updatedAt - this.prevUpdatedAt, Bh);
    return Wv(parseFloat(this.current) - parseFloat(this.prevFrameValue), n);
  }
  start(t) {
    return (
      this.stop(),
      new Promise((n) => {
        (this.hasAnimated = !0),
          (this.animation = t(n)),
          this.events.animationStart && this.events.animationStart.notify();
      }).then(() => {
        this.events.animationComplete && this.events.animationComplete.notify(),
          this.clearAnimation();
      })
    );
  }
  stop() {
    this.animation &&
      (this.animation.stop(),
      this.events.animationCancel && this.events.animationCancel.notify()),
      this.clearAnimation();
  }
  isAnimating() {
    return !!this.animation;
  }
  clearAnimation() {
    delete this.animation;
  }
  destroy() {
    this.clearListeners(),
      this.stop(),
      this.stopPassiveEffect && this.stopPassiveEffect();
  }
}
function xs(e, t) {
  return new gT(e, t);
}
function yT(e, t, n) {
  e.hasValue(t) ? e.getValue(t).set(n) : e.addValue(t, xs(n));
}
function vT(e, t) {
  const n = Da(e, t);
  let { transitionEnd: r = {}, transition: i = {}, ...s } = n || {};
  s = { ...s, ...r };
  for (const o in s) {
    const a = pT(s[o]);
    yT(e, o, a);
  }
}
const Pd = (e) => e.replace(/([a-z])([A-Z])/gu, "$1-$2").toLowerCase(),
  xT = "framerAppearId",
  e0 = "data-" + Pd(xT);
function t0(e) {
  return e.props[e0];
}
const je = (e) => !!(e && e.getVelocity);
function wT(e) {
  return !!(je(e) && e.add);
}
function Uu(e, t) {
  const n = e.getValue("willChange");
  if (wT(n)) return n.add(t);
}
function ST({ protectedKeys: e, needsAnimating: t }, n) {
  const r = e.hasOwnProperty(n) && t[n] !== !0;
  return (t[n] = !1), r;
}
function n0(e, t, { delay: n = 0, transitionOverride: r, type: i } = {}) {
  var s;
  let { transition: o = e.getDefaultTransition(), transitionEnd: a, ...l } = t;
  r && (o = r);
  const u = [],
    c = i && e.animationState && e.animationState.getState()[i];
  for (const d in l) {
    const f = e.getValue(
        d,
        (s = e.latestValues[d]) !== null && s !== void 0 ? s : null
      ),
      v = l[d];
    if (v === void 0 || (c && ST(c, d))) continue;
    const y = { delay: n, ...id(o || {}, d) };
    let m = !1;
    if (window.MotionHandoffAnimation) {
      const h = t0(e);
      if (h) {
        const p = window.MotionHandoffAnimation(h, d, Y);
        p !== null && ((y.startTime = p), (m = !0));
      }
    }
    Uu(e, d),
      f.start(
        vd(d, f, v, e.shouldReduceMotion && wr.has(d) ? { type: !1 } : y, e, m)
      );
    const x = f.animation;
    x && u.push(x);
  }
  return (
    a &&
      Promise.all(u).then(() => {
        Y.update(() => {
          a && vT(e, a);
        });
      }),
    u
  );
}
function $u(e, t, n = {}) {
  var r;
  const i = Da(
    e,
    t,
    n.type === "exit"
      ? (r = e.presenceContext) === null || r === void 0
        ? void 0
        : r.custom
      : void 0
  );
  let { transition: s = e.getDefaultTransition() || {} } = i || {};
  n.transitionOverride && (s = n.transitionOverride);
  const o = i ? () => Promise.all(n0(e, i, n)) : () => Promise.resolve(),
    a =
      e.variantChildren && e.variantChildren.size
        ? (u = 0) => {
            const {
              delayChildren: c = 0,
              staggerChildren: d,
              staggerDirection: f,
            } = s;
            return PT(e, t, c + u, d, f, n);
          }
        : () => Promise.resolve(),
    { when: l } = s;
  if (l) {
    const [u, c] = l === "beforeChildren" ? [o, a] : [a, o];
    return u().then(() => c());
  } else return Promise.all([o(), a(n.delay)]);
}
function PT(e, t, n = 0, r = 0, i = 1, s) {
  const o = [],
    a = (e.variantChildren.size - 1) * r,
    l = i === 1 ? (u = 0) => u * r : (u = 0) => a - u * r;
  return (
    Array.from(e.variantChildren)
      .sort(CT)
      .forEach((u, c) => {
        u.notify("AnimationStart", t),
          o.push(
            $u(u, t, { ...s, delay: n + l(c) }).then(() =>
              u.notify("AnimationComplete", t)
            )
          );
      }),
    Promise.all(o)
  );
}
function CT(e, t) {
  return e.sortNodePosition(t);
}
function ET(e, t, n = {}) {
  e.notify("AnimationStart", t);
  let r;
  if (Array.isArray(t)) {
    const i = t.map((s) => $u(e, s, n));
    r = Promise.all(i);
  } else if (typeof t == "string") r = $u(e, t, n);
  else {
    const i = typeof t == "function" ? Da(e, t, n.custom) : t;
    r = Promise.all(n0(e, i, n));
  }
  return r.then(() => {
    e.notify("AnimationComplete", t);
  });
}
const TT = rd.length;
function r0(e) {
  if (!e) return;
  if (!e.isControllingVariants) {
    const n = e.parent ? r0(e.parent) || {} : {};
    return e.props.initial !== void 0 && (n.initial = e.props.initial), n;
  }
  const t = {};
  for (let n = 0; n < TT; n++) {
    const r = rd[n],
      i = e.props[r];
    (gs(i) || i === !1) && (t[r] = i);
  }
  return t;
}
const kT = [...nd].reverse(),
  AT = nd.length;
function RT(e) {
  return (t) =>
    Promise.all(t.map(({ animation: n, options: r }) => ET(e, n, r)));
}
function MT(e) {
  let t = RT(e),
    n = Uh(),
    r = !0;
  const i = (l) => (u, c) => {
    var d;
    const f = Da(
      e,
      c,
      l === "exit"
        ? (d = e.presenceContext) === null || d === void 0
          ? void 0
          : d.custom
        : void 0
    );
    if (f) {
      const { transition: v, transitionEnd: y, ...m } = f;
      u = { ...u, ...m, ...y };
    }
    return u;
  };
  function s(l) {
    t = l(e);
  }
  function o(l) {
    const { props: u } = e,
      c = r0(e.parent) || {},
      d = [],
      f = new Set();
    let v = {},
      y = 1 / 0;
    for (let x = 0; x < AT; x++) {
      const h = kT[x],
        p = n[h],
        g = u[h] !== void 0 ? u[h] : c[h],
        S = gs(g),
        C = h === l ? p.isActive : null;
      C === !1 && (y = x);
      let k = g === c[h] && g !== u[h] && S;
      if (
        (k && r && e.manuallyAnimateOnMount && (k = !1),
        (p.protectedKeys = { ...v }),
        (!p.isActive && C === null) ||
          (!g && !p.prevProp) ||
          Ma(g) ||
          typeof g == "boolean")
      )
        continue;
      const T = DT(p.prevProp, g);
      let E = T || (h === l && p.isActive && !k && S) || (x > y && S),
        D = !1;
      const N = Array.isArray(g) ? g : [g];
      let j = N.reduce(i(h), {});
      C === !1 && (j = {});
      const { prevResolvedValues: I = {} } = p,
        Z = { ...I, ...j },
        b = (B) => {
          (E = !0),
            f.has(B) && ((D = !0), f.delete(B)),
            (p.needsAnimating[B] = !0);
          const R = e.getValue(B);
          R && (R.liveStyle = !1);
        };
      for (const B in Z) {
        const R = j[B],
          L = I[B];
        if (v.hasOwnProperty(B)) continue;
        let F = !1;
        bu(R) && bu(L) ? (F = !gv(R, L)) : (F = R !== L),
          F
            ? R != null
              ? b(B)
              : f.add(B)
            : R !== void 0 && f.has(B)
            ? b(B)
            : (p.protectedKeys[B] = !0);
      }
      (p.prevProp = g),
        (p.prevResolvedValues = j),
        p.isActive && (v = { ...v, ...j }),
        r && e.blockInitialAnimation && (E = !1),
        E &&
          (!(k && T) || D) &&
          d.push(...N.map((B) => ({ animation: B, options: { type: h } })));
    }
    if (f.size) {
      const x = {};
      f.forEach((h) => {
        const p = e.getBaseTarget(h),
          g = e.getValue(h);
        g && (g.liveStyle = !0), (x[h] = p ?? null);
      }),
        d.push({ animation: x });
    }
    let m = !!d.length;
    return (
      r &&
        (u.initial === !1 || u.initial === u.animate) &&
        !e.manuallyAnimateOnMount &&
        (m = !1),
      (r = !1),
      m ? t(d) : Promise.resolve()
    );
  }
  function a(l, u) {
    var c;
    if (n[l].isActive === u) return Promise.resolve();
    (c = e.variantChildren) === null ||
      c === void 0 ||
      c.forEach((f) => {
        var v;
        return (v = f.animationState) === null || v === void 0
          ? void 0
          : v.setActive(l, u);
      }),
      (n[l].isActive = u);
    const d = o(l);
    for (const f in n) n[f].protectedKeys = {};
    return d;
  }
  return {
    animateChanges: o,
    setActive: a,
    setAnimateFunction: s,
    getState: () => n,
    reset: () => {
      (n = Uh()), (r = !0);
    },
  };
}
function DT(e, t) {
  return typeof t == "string" ? t !== e : Array.isArray(t) ? !gv(t, e) : !1;
}
function Gn(e = !1) {
  return {
    isActive: e,
    protectedKeys: {},
    needsAnimating: {},
    prevResolvedValues: {},
  };
}
function Uh() {
  return {
    animate: Gn(!0),
    whileInView: Gn(),
    whileHover: Gn(),
    whileTap: Gn(),
    whileDrag: Gn(),
    whileFocus: Gn(),
    exit: Gn(),
  };
}
class Kn {
  constructor(t) {
    (this.isMounted = !1), (this.node = t);
  }
  update() {}
}
class NT extends Kn {
  constructor(t) {
    super(t), t.animationState || (t.animationState = MT(t));
  }
  updateAnimationControlsSubscription() {
    const { animate: t } = this.node.getProps();
    Ma(t) && (this.unmountControls = t.subscribe(this.node));
  }
  mount() {
    this.updateAnimationControlsSubscription();
  }
  update() {
    const { animate: t } = this.node.getProps(),
      { animate: n } = this.node.prevProps || {};
    t !== n && this.updateAnimationControlsSubscription();
  }
  unmount() {
    var t;
    this.node.animationState.reset(),
      (t = this.unmountControls) === null || t === void 0 || t.call(this);
  }
}
let bT = 0;
class LT extends Kn {
  constructor() {
    super(...arguments), (this.id = bT++);
  }
  update() {
    if (!this.node.presenceContext) return;
    const { isPresent: t, onExitComplete: n } = this.node.presenceContext,
      { isPresent: r } = this.node.prevPresenceContext || {};
    if (!this.node.animationState || t === r) return;
    const i = this.node.animationState.setActive("exit", !t);
    n && !t && i.then(() => n(this.id));
  }
  mount() {
    const { register: t } = this.node.presenceContext || {};
    t && (this.unmount = t(this.id));
  }
  unmount() {}
}
const OT = { animation: { Feature: NT }, exit: { Feature: LT } };
function jT(e, t, n) {
  var r;
  if (e instanceof Element) return [e];
  if (typeof e == "string") {
    let i = document;
    const s = (r = void 0) !== null && r !== void 0 ? r : i.querySelectorAll(e);
    return s ? Array.from(s) : [];
  }
  return Array.from(e);
}
const wt = { x: !1, y: !1 };
function i0() {
  return wt.x || wt.y;
}
function $h(e) {
  return (t) => {
    t.pointerType === "touch" || i0() || e(t);
  };
}
function IT(e, t, n = {}) {
  const r = new AbortController(),
    i = { passive: !0, ...n, signal: r.signal },
    s = $h((o) => {
      const { target: a } = o,
        l = t(o);
      if (!l || !a) return;
      const u = $h((c) => {
        l(c), a.removeEventListener("pointerleave", u);
      });
      a.addEventListener("pointerleave", u, i);
    });
  return (
    jT(e).forEach((o) => {
      o.addEventListener("pointerenter", s, i);
    }),
    () => r.abort()
  );
}
function FT(e) {
  return e === "x" || e === "y"
    ? wt[e]
      ? null
      : ((wt[e] = !0),
        () => {
          wt[e] = !1;
        })
    : wt.x || wt.y
    ? null
    : ((wt.x = wt.y = !0),
      () => {
        wt.x = wt.y = !1;
      });
}
const s0 = (e) =>
  e.pointerType === "mouse"
    ? typeof e.button != "number" || e.button <= 0
    : e.isPrimary !== !1;
function Ls(e) {
  return { point: { x: e.pageX, y: e.pageY } };
}
const _T = (e) => (t) => s0(t) && e(t, Ls(t));
function Yt(e, t, n, r = { passive: !0 }) {
  return e.addEventListener(t, n, r), () => e.removeEventListener(t, n);
}
function _n(e, t, n, r) {
  return Yt(e, t, _T(n), r);
}
const Wh = (e, t) => Math.abs(e - t);
function VT(e, t) {
  const n = Wh(e.x, t.x),
    r = Wh(e.y, t.y);
  return Math.sqrt(n ** 2 + r ** 2);
}
class o0 {
  constructor(
    t,
    n,
    { transformPagePoint: r, contextWindow: i, dragSnapToOrigin: s = !1 } = {}
  ) {
    if (
      ((this.startEvent = null),
      (this.lastMoveEvent = null),
      (this.lastMoveEventInfo = null),
      (this.handlers = {}),
      (this.contextWindow = window),
      (this.updatePoint = () => {
        if (!(this.lastMoveEvent && this.lastMoveEventInfo)) return;
        const d = kl(this.lastMoveEventInfo, this.history),
          f = this.startEvent !== null,
          v = VT(d.offset, { x: 0, y: 0 }) >= 3;
        if (!f && !v) return;
        const { point: y } = d,
          { timestamp: m } = ke;
        this.history.push({ ...y, timestamp: m });
        const { onStart: x, onMove: h } = this.handlers;
        f ||
          (x && x(this.lastMoveEvent, d),
          (this.startEvent = this.lastMoveEvent)),
          h && h(this.lastMoveEvent, d);
      }),
      (this.handlePointerMove = (d, f) => {
        (this.lastMoveEvent = d),
          (this.lastMoveEventInfo = Tl(f, this.transformPagePoint)),
          Y.update(this.updatePoint, !0);
      }),
      (this.handlePointerUp = (d, f) => {
        this.end();
        const { onEnd: v, onSessionEnd: y, resumeAnimation: m } = this.handlers;
        if (
          (this.dragSnapToOrigin && m && m(),
          !(this.lastMoveEvent && this.lastMoveEventInfo))
        )
          return;
        const x = kl(
          d.type === "pointercancel"
            ? this.lastMoveEventInfo
            : Tl(f, this.transformPagePoint),
          this.history
        );
        this.startEvent && v && v(d, x), y && y(d, x);
      }),
      !s0(t))
    )
      return;
    (this.dragSnapToOrigin = s),
      (this.handlers = n),
      (this.transformPagePoint = r),
      (this.contextWindow = i || window);
    const o = Ls(t),
      a = Tl(o, this.transformPagePoint),
      { point: l } = a,
      { timestamp: u } = ke;
    this.history = [{ ...l, timestamp: u }];
    const { onSessionStart: c } = n;
    c && c(t, kl(a, this.history)),
      (this.removeListeners = Fn(
        _n(this.contextWindow, "pointermove", this.handlePointerMove),
        _n(this.contextWindow, "pointerup", this.handlePointerUp),
        _n(this.contextWindow, "pointercancel", this.handlePointerUp)
      ));
  }
  updateHandlers(t) {
    this.handlers = t;
  }
  end() {
    this.removeListeners && this.removeListeners(), Bn(this.updatePoint);
  }
}
function Tl(e, t) {
  return t ? { point: t(e.point) } : e;
}
function Hh(e, t) {
  return { x: e.x - t.x, y: e.y - t.y };
}
function kl({ point: e }, t) {
  return {
    point: e,
    delta: Hh(e, a0(t)),
    offset: Hh(e, zT(t)),
    velocity: BT(t, 0.1),
  };
}
function zT(e) {
  return e[0];
}
function a0(e) {
  return e[e.length - 1];
}
function BT(e, t) {
  if (e.length < 2) return { x: 0, y: 0 };
  let n = e.length - 1,
    r = null;
  const i = a0(e);
  for (; n >= 0 && ((r = e[n]), !(i.timestamp - r.timestamp > Jt(t))); ) n--;
  if (!r) return { x: 0, y: 0 };
  const s = en(i.timestamp - r.timestamp);
  if (s === 0) return { x: 0, y: 0 };
  const o = { x: (i.x - r.x) / s, y: (i.y - r.y) / s };
  return o.x === 1 / 0 && (o.x = 0), o.y === 1 / 0 && (o.y = 0), o;
}
function jr(e) {
  return (
    e &&
    typeof e == "object" &&
    Object.prototype.hasOwnProperty.call(e, "current")
  );
}
const l0 = 1e-4,
  UT = 1 - l0,
  $T = 1 + l0,
  u0 = 0.01,
  WT = 0 - u0,
  HT = 0 + u0;
function it(e) {
  return e.max - e.min;
}
function KT(e, t, n) {
  return Math.abs(e - t) <= n;
}
function Kh(e, t, n, r = 0.5) {
  (e.origin = r),
    (e.originPoint = ae(t.min, t.max, e.origin)),
    (e.scale = it(n) / it(t)),
    (e.translate = ae(n.min, n.max, e.origin) - e.originPoint),
    ((e.scale >= UT && e.scale <= $T) || isNaN(e.scale)) && (e.scale = 1),
    ((e.translate >= WT && e.translate <= HT) || isNaN(e.translate)) &&
      (e.translate = 0);
}
function Qi(e, t, n, r) {
  Kh(e.x, t.x, n.x, r ? r.originX : void 0),
    Kh(e.y, t.y, n.y, r ? r.originY : void 0);
}
function Qh(e, t, n) {
  (e.min = n.min + t.min), (e.max = e.min + it(t));
}
function QT(e, t, n) {
  Qh(e.x, t.x, n.x), Qh(e.y, t.y, n.y);
}
function Gh(e, t, n) {
  (e.min = t.min - n.min), (e.max = e.min + it(t));
}
function Gi(e, t, n) {
  Gh(e.x, t.x, n.x), Gh(e.y, t.y, n.y);
}
function GT(e, { min: t, max: n }, r) {
  return (
    t !== void 0 && e < t
      ? (e = r ? ae(t, e, r.min) : Math.max(e, t))
      : n !== void 0 && e > n && (e = r ? ae(n, e, r.max) : Math.min(e, n)),
    e
  );
}
function qh(e, t, n) {
  return {
    min: t !== void 0 ? e.min + t : void 0,
    max: n !== void 0 ? e.max + n - (e.max - e.min) : void 0,
  };
}
function qT(e, { top: t, left: n, bottom: r, right: i }) {
  return { x: qh(e.x, n, i), y: qh(e.y, t, r) };
}
function Xh(e, t) {
  let n = t.min - e.min,
    r = t.max - e.max;
  return t.max - t.min < e.max - e.min && ([n, r] = [r, n]), { min: n, max: r };
}
function XT(e, t) {
  return { x: Xh(e.x, t.x), y: Xh(e.y, t.y) };
}
function YT(e, t) {
  let n = 0.5;
  const r = it(e),
    i = it(t);
  return (
    i > r
      ? (n = ci(t.min, t.max - r, e.min))
      : r > i && (n = ci(e.min, e.max - i, t.min)),
    an(0, 1, n)
  );
}
function ZT(e, t) {
  const n = {};
  return (
    t.min !== void 0 && (n.min = t.min - e.min),
    t.max !== void 0 && (n.max = t.max - e.min),
    n
  );
}
const Wu = 0.35;
function JT(e = Wu) {
  return (
    e === !1 ? (e = 0) : e === !0 && (e = Wu),
    { x: Yh(e, "left", "right"), y: Yh(e, "top", "bottom") }
  );
}
function Yh(e, t, n) {
  return { min: Zh(e, t), max: Zh(e, n) };
}
function Zh(e, t) {
  return typeof e == "number" ? e : e[t] || 0;
}
const Jh = () => ({ translate: 0, scale: 1, origin: 0, originPoint: 0 }),
  Ir = () => ({ x: Jh(), y: Jh() }),
  ep = () => ({ min: 0, max: 0 }),
  pe = () => ({ x: ep(), y: ep() });
function ct(e) {
  return [e("x"), e("y")];
}
function c0({ top: e, left: t, right: n, bottom: r }) {
  return { x: { min: t, max: n }, y: { min: e, max: r } };
}
function ek({ x: e, y: t }) {
  return { top: t.min, right: e.max, bottom: t.max, left: e.min };
}
function tk(e, t) {
  if (!t) return e;
  const n = t({ x: e.left, y: e.top }),
    r = t({ x: e.right, y: e.bottom });
  return { top: n.y, left: n.x, bottom: r.y, right: r.x };
}
function Al(e) {
  return e === void 0 || e === 1;
}
function Hu({ scale: e, scaleX: t, scaleY: n }) {
  return !Al(e) || !Al(t) || !Al(n);
}
function Yn(e) {
  return (
    Hu(e) ||
    d0(e) ||
    e.z ||
    e.rotate ||
    e.rotateX ||
    e.rotateY ||
    e.skewX ||
    e.skewY
  );
}
function d0(e) {
  return tp(e.x) || tp(e.y);
}
function tp(e) {
  return e && e !== "0%";
}
function ea(e, t, n) {
  const r = e - n,
    i = t * r;
  return n + i;
}
function np(e, t, n, r, i) {
  return i !== void 0 && (e = ea(e, i, r)), ea(e, n, r) + t;
}
function Ku(e, t = 0, n = 1, r, i) {
  (e.min = np(e.min, t, n, r, i)), (e.max = np(e.max, t, n, r, i));
}
function f0(e, { x: t, y: n }) {
  Ku(e.x, t.translate, t.scale, t.originPoint),
    Ku(e.y, n.translate, n.scale, n.originPoint);
}
const rp = 0.999999999999,
  ip = 1.0000000000001;
function nk(e, t, n, r = !1) {
  const i = n.length;
  if (!i) return;
  t.x = t.y = 1;
  let s, o;
  for (let a = 0; a < i; a++) {
    (s = n[a]), (o = s.projectionDelta);
    const { visualElement: l } = s.options;
    (l && l.props.style && l.props.style.display === "contents") ||
      (r &&
        s.options.layoutScroll &&
        s.scroll &&
        s !== s.root &&
        _r(e, { x: -s.scroll.offset.x, y: -s.scroll.offset.y }),
      o && ((t.x *= o.x.scale), (t.y *= o.y.scale), f0(e, o)),
      r && Yn(s.latestValues) && _r(e, s.latestValues));
  }
  t.x < ip && t.x > rp && (t.x = 1), t.y < ip && t.y > rp && (t.y = 1);
}
function Fr(e, t) {
  (e.min = e.min + t), (e.max = e.max + t);
}
function sp(e, t, n, r, i = 0.5) {
  const s = ae(e.min, e.max, i);
  Ku(e, t, n, s, r);
}
function _r(e, t) {
  sp(e.x, t.x, t.scaleX, t.scale, t.originX),
    sp(e.y, t.y, t.scaleY, t.scale, t.originY);
}
function h0(e, t) {
  return c0(tk(e.getBoundingClientRect(), t));
}
function rk(e, t, n) {
  const r = h0(e, n),
    { scroll: i } = t;
  return i && (Fr(r.x, i.offset.x), Fr(r.y, i.offset.y)), r;
}
const p0 = ({ current: e }) => (e ? e.ownerDocument.defaultView : null),
  ik = new WeakMap();
class sk {
  constructor(t) {
    (this.openDragLock = null),
      (this.isDragging = !1),
      (this.currentDirection = null),
      (this.originPoint = { x: 0, y: 0 }),
      (this.constraints = !1),
      (this.hasMutatedConstraints = !1),
      (this.elastic = pe()),
      (this.visualElement = t);
  }
  start(t, { snapToCursor: n = !1 } = {}) {
    const { presenceContext: r } = this.visualElement;
    if (r && r.isPresent === !1) return;
    const i = (c) => {
        const { dragSnapToOrigin: d } = this.getProps();
        d ? this.pauseAnimation() : this.stopAnimation(),
          n && this.snapToCursor(Ls(c).point);
      },
      s = (c, d) => {
        const { drag: f, dragPropagation: v, onDragStart: y } = this.getProps();
        if (
          f &&
          !v &&
          (this.openDragLock && this.openDragLock(),
          (this.openDragLock = FT(f)),
          !this.openDragLock)
        )
          return;
        (this.isDragging = !0),
          (this.currentDirection = null),
          this.resolveConstraints(),
          this.visualElement.projection &&
            ((this.visualElement.projection.isAnimationBlocked = !0),
            (this.visualElement.projection.target = void 0)),
          ct((x) => {
            let h = this.getAxisMotionValue(x).get() || 0;
            if (Vt.test(h)) {
              const { projection: p } = this.visualElement;
              if (p && p.layout) {
                const g = p.layout.layoutBox[x];
                g && (h = it(g) * (parseFloat(h) / 100));
              }
            }
            this.originPoint[x] = h;
          }),
          y && Y.postRender(() => y(c, d)),
          Uu(this.visualElement, "transform");
        const { animationState: m } = this.visualElement;
        m && m.setActive("whileDrag", !0);
      },
      o = (c, d) => {
        const {
          dragPropagation: f,
          dragDirectionLock: v,
          onDirectionLock: y,
          onDrag: m,
        } = this.getProps();
        if (!f && !this.openDragLock) return;
        const { offset: x } = d;
        if (v && this.currentDirection === null) {
          (this.currentDirection = ok(x)),
            this.currentDirection !== null && y && y(this.currentDirection);
          return;
        }
        this.updateAxis("x", d.point, x),
          this.updateAxis("y", d.point, x),
          this.visualElement.render(),
          m && m(c, d);
      },
      a = (c, d) => this.stop(c, d),
      l = () =>
        ct((c) => {
          var d;
          return (
            this.getAnimationState(c) === "paused" &&
            ((d = this.getAxisMotionValue(c).animation) === null || d === void 0
              ? void 0
              : d.play())
          );
        }),
      { dragSnapToOrigin: u } = this.getProps();
    this.panSession = new o0(
      t,
      {
        onSessionStart: i,
        onStart: s,
        onMove: o,
        onSessionEnd: a,
        resumeAnimation: l,
      },
      {
        transformPagePoint: this.visualElement.getTransformPagePoint(),
        dragSnapToOrigin: u,
        contextWindow: p0(this.visualElement),
      }
    );
  }
  stop(t, n) {
    const r = this.isDragging;
    if ((this.cancel(), !r)) return;
    const { velocity: i } = n;
    this.startAnimation(i);
    const { onDragEnd: s } = this.getProps();
    s && Y.postRender(() => s(t, n));
  }
  cancel() {
    this.isDragging = !1;
    const { projection: t, animationState: n } = this.visualElement;
    t && (t.isAnimationBlocked = !1),
      this.panSession && this.panSession.end(),
      (this.panSession = void 0);
    const { dragPropagation: r } = this.getProps();
    !r &&
      this.openDragLock &&
      (this.openDragLock(), (this.openDragLock = null)),
      n && n.setActive("whileDrag", !1);
  }
  updateAxis(t, n, r) {
    const { drag: i } = this.getProps();
    if (!r || !so(t, i, this.currentDirection)) return;
    const s = this.getAxisMotionValue(t);
    let o = this.originPoint[t] + r[t];
    this.constraints &&
      this.constraints[t] &&
      (o = GT(o, this.constraints[t], this.elastic[t])),
      s.set(o);
  }
  resolveConstraints() {
    var t;
    const { dragConstraints: n, dragElastic: r } = this.getProps(),
      i =
        this.visualElement.projection && !this.visualElement.projection.layout
          ? this.visualElement.projection.measure(!1)
          : (t = this.visualElement.projection) === null || t === void 0
          ? void 0
          : t.layout,
      s = this.constraints;
    n && jr(n)
      ? this.constraints || (this.constraints = this.resolveRefConstraints())
      : n && i
      ? (this.constraints = qT(i.layoutBox, n))
      : (this.constraints = !1),
      (this.elastic = JT(r)),
      s !== this.constraints &&
        i &&
        this.constraints &&
        !this.hasMutatedConstraints &&
        ct((o) => {
          this.constraints !== !1 &&
            this.getAxisMotionValue(o) &&
            (this.constraints[o] = ZT(i.layoutBox[o], this.constraints[o]));
        });
  }
  resolveRefConstraints() {
    const { dragConstraints: t, onMeasureDragConstraints: n } = this.getProps();
    if (!t || !jr(t)) return !1;
    const r = t.current,
      { projection: i } = this.visualElement;
    if (!i || !i.layout) return !1;
    const s = rk(r, i.root, this.visualElement.getTransformPagePoint());
    let o = XT(i.layout.layoutBox, s);
    if (n) {
      const a = n(ek(o));
      (this.hasMutatedConstraints = !!a), a && (o = c0(a));
    }
    return o;
  }
  startAnimation(t) {
    const {
        drag: n,
        dragMomentum: r,
        dragElastic: i,
        dragTransition: s,
        dragSnapToOrigin: o,
        onDragTransitionEnd: a,
      } = this.getProps(),
      l = this.constraints || {},
      u = ct((c) => {
        if (!so(c, n, this.currentDirection)) return;
        let d = (l && l[c]) || {};
        o && (d = { min: 0, max: 0 });
        const f = i ? 200 : 1e6,
          v = i ? 40 : 1e7,
          y = {
            type: "inertia",
            velocity: r ? t[c] : 0,
            bounceStiffness: f,
            bounceDamping: v,
            timeConstant: 750,
            restDelta: 1,
            restSpeed: 10,
            ...s,
            ...d,
          };
        return this.startAxisValueAnimation(c, y);
      });
    return Promise.all(u).then(a);
  }
  startAxisValueAnimation(t, n) {
    const r = this.getAxisMotionValue(t);
    return (
      Uu(this.visualElement, t), r.start(vd(t, r, 0, n, this.visualElement, !1))
    );
  }
  stopAnimation() {
    ct((t) => this.getAxisMotionValue(t).stop());
  }
  pauseAnimation() {
    ct((t) => {
      var n;
      return (n = this.getAxisMotionValue(t).animation) === null || n === void 0
        ? void 0
        : n.pause();
    });
  }
  getAnimationState(t) {
    var n;
    return (n = this.getAxisMotionValue(t).animation) === null || n === void 0
      ? void 0
      : n.state;
  }
  getAxisMotionValue(t) {
    const n = `_drag${t.toUpperCase()}`,
      r = this.visualElement.getProps(),
      i = r[n];
    return (
      i ||
      this.visualElement.getValue(t, (r.initial ? r.initial[t] : void 0) || 0)
    );
  }
  snapToCursor(t) {
    ct((n) => {
      const { drag: r } = this.getProps();
      if (!so(n, r, this.currentDirection)) return;
      const { projection: i } = this.visualElement,
        s = this.getAxisMotionValue(n);
      if (i && i.layout) {
        const { min: o, max: a } = i.layout.layoutBox[n];
        s.set(t[n] - ae(o, a, 0.5));
      }
    });
  }
  scalePositionWithinConstraints() {
    if (!this.visualElement.current) return;
    const { drag: t, dragConstraints: n } = this.getProps(),
      { projection: r } = this.visualElement;
    if (!jr(n) || !r || !this.constraints) return;
    this.stopAnimation();
    const i = { x: 0, y: 0 };
    ct((o) => {
      const a = this.getAxisMotionValue(o);
      if (a && this.constraints !== !1) {
        const l = a.get();
        i[o] = YT({ min: l, max: l }, this.constraints[o]);
      }
    });
    const { transformTemplate: s } = this.visualElement.getProps();
    (this.visualElement.current.style.transform = s ? s({}, "") : "none"),
      r.root && r.root.updateScroll(),
      r.updateLayout(),
      this.resolveConstraints(),
      ct((o) => {
        if (!so(o, t, null)) return;
        const a = this.getAxisMotionValue(o),
          { min: l, max: u } = this.constraints[o];
        a.set(ae(l, u, i[o]));
      });
  }
  addListeners() {
    if (!this.visualElement.current) return;
    ik.set(this.visualElement, this);
    const t = this.visualElement.current,
      n = _n(t, "pointerdown", (l) => {
        const { drag: u, dragListener: c = !0 } = this.getProps();
        u && c && this.start(l);
      }),
      r = () => {
        const { dragConstraints: l } = this.getProps();
        jr(l) && l.current && (this.constraints = this.resolveRefConstraints());
      },
      { projection: i } = this.visualElement,
      s = i.addEventListener("measure", r);
    i && !i.layout && (i.root && i.root.updateScroll(), i.updateLayout()),
      Y.read(r);
    const o = Yt(window, "resize", () => this.scalePositionWithinConstraints()),
      a = i.addEventListener(
        "didUpdate",
        ({ delta: l, hasLayoutChanged: u }) => {
          this.isDragging &&
            u &&
            (ct((c) => {
              const d = this.getAxisMotionValue(c);
              d &&
                ((this.originPoint[c] += l[c].translate),
                d.set(d.get() + l[c].translate));
            }),
            this.visualElement.render());
        }
      );
    return () => {
      o(), n(), s(), a && a();
    };
  }
  getProps() {
    const t = this.visualElement.getProps(),
      {
        drag: n = !1,
        dragDirectionLock: r = !1,
        dragPropagation: i = !1,
        dragConstraints: s = !1,
        dragElastic: o = Wu,
        dragMomentum: a = !0,
      } = t;
    return {
      ...t,
      drag: n,
      dragDirectionLock: r,
      dragPropagation: i,
      dragConstraints: s,
      dragElastic: o,
      dragMomentum: a,
    };
  }
}
function so(e, t, n) {
  return (t === !0 || t === e) && (n === null || n === e);
}
function ok(e, t = 10) {
  let n = null;
  return Math.abs(e.y) > t ? (n = "y") : Math.abs(e.x) > t && (n = "x"), n;
}
class ak extends Kn {
  constructor(t) {
    super(t),
      (this.removeGroupControls = Ie),
      (this.removeListeners = Ie),
      (this.controls = new sk(t));
  }
  mount() {
    const { dragControls: t } = this.node.getProps();
    t && (this.removeGroupControls = t.subscribe(this.controls)),
      (this.removeListeners = this.controls.addListeners() || Ie);
  }
  unmount() {
    this.removeGroupControls(), this.removeListeners();
  }
}
const op = (e) => (t, n) => {
  e && Y.postRender(() => e(t, n));
};
class lk extends Kn {
  constructor() {
    super(...arguments), (this.removePointerDownListener = Ie);
  }
  onPointerDown(t) {
    this.session = new o0(t, this.createPanHandlers(), {
      transformPagePoint: this.node.getTransformPagePoint(),
      contextWindow: p0(this.node),
    });
  }
  createPanHandlers() {
    const {
      onPanSessionStart: t,
      onPanStart: n,
      onPan: r,
      onPanEnd: i,
    } = this.node.getProps();
    return {
      onSessionStart: op(t),
      onStart: op(n),
      onMove: r,
      onEnd: (s, o) => {
        delete this.session, i && Y.postRender(() => i(s, o));
      },
    };
  }
  mount() {
    this.removePointerDownListener = _n(this.node.current, "pointerdown", (t) =>
      this.onPointerDown(t)
    );
  }
  update() {
    this.session && this.session.updateHandlers(this.createPanHandlers());
  }
  unmount() {
    this.removePointerDownListener(), this.session && this.session.end();
  }
}
const Cd = w.createContext(null);
function uk() {
  const e = w.useContext(Cd);
  if (e === null) return [!0, null];
  const { isPresent: t, onExitComplete: n, register: r } = e,
    i = w.useId();
  w.useEffect(() => r(i), []);
  const s = w.useCallback(() => n && n(i), [i, n]);
  return !t && n ? [!1, s] : [!0];
}
const m0 = w.createContext({}),
  g0 = w.createContext({}),
  Po = { hasAnimatedSinceResize: !0, hasEverUpdated: !1 };
function ap(e, t) {
  return t.max === t.min ? 0 : (e / (t.max - t.min)) * 100;
}
const Ri = {
    correct: (e, t) => {
      if (!t.target) return e;
      if (typeof e == "string")
        if (V.test(e)) e = parseFloat(e);
        else return e;
      const n = ap(e, t.target.x),
        r = ap(e, t.target.y);
      return `${n}% ${r}%`;
    },
  },
  ck = {
    correct: (e, { treeScale: t, projectionDelta: n }) => {
      const r = e,
        i = Un.parse(e);
      if (i.length > 5) return r;
      const s = Un.createTransformer(e),
        o = typeof i[0] != "number" ? 1 : 0,
        a = n.x.scale * t.x,
        l = n.y.scale * t.y;
      (i[0 + o] /= a), (i[1 + o] /= l);
      const u = ae(a, l, 0.5);
      return (
        typeof i[2 + o] == "number" && (i[2 + o] /= u),
        typeof i[3 + o] == "number" && (i[3 + o] /= u),
        s(i)
      );
    },
  },
  ta = {};
function dk(e) {
  Object.assign(ta, e);
}
const { schedule: Ed, cancel: HR } = yv(queueMicrotask, !1);
class fk extends w.Component {
  componentDidMount() {
    const {
        visualElement: t,
        layoutGroup: n,
        switchLayoutGroup: r,
        layoutId: i,
      } = this.props,
      { projection: s } = t;
    dk(hk),
      s &&
        (n.group && n.group.add(s),
        r && r.register && i && r.register(s),
        s.root.didUpdate(),
        s.addEventListener("animationComplete", () => {
          this.safeToRemove();
        }),
        s.setOptions({
          ...s.options,
          onExitComplete: () => this.safeToRemove(),
        })),
      (Po.hasEverUpdated = !0);
  }
  getSnapshotBeforeUpdate(t) {
    const {
        layoutDependency: n,
        visualElement: r,
        drag: i,
        isPresent: s,
      } = this.props,
      o = r.projection;
    return (
      o &&
        ((o.isPresent = s),
        i || t.layoutDependency !== n || n === void 0
          ? o.willUpdate()
          : this.safeToRemove(),
        t.isPresent !== s &&
          (s
            ? o.promote()
            : o.relegate() ||
              Y.postRender(() => {
                const a = o.getStack();
                (!a || !a.members.length) && this.safeToRemove();
              }))),
      null
    );
  }
  componentDidUpdate() {
    const { projection: t } = this.props.visualElement;
    t &&
      (t.root.didUpdate(),
      Ed.postRender(() => {
        !t.currentAnimation && t.isLead() && this.safeToRemove();
      }));
  }
  componentWillUnmount() {
    const {
        visualElement: t,
        layoutGroup: n,
        switchLayoutGroup: r,
      } = this.props,
      { projection: i } = t;
    i &&
      (i.scheduleCheckAfterUnmount(),
      n && n.group && n.group.remove(i),
      r && r.deregister && r.deregister(i));
  }
  safeToRemove() {
    const { safeToRemove: t } = this.props;
    t && t();
  }
  render() {
    return null;
  }
}
function y0(e) {
  const [t, n] = uk(),
    r = w.useContext(m0);
  return P.jsx(fk, {
    ...e,
    layoutGroup: r,
    switchLayoutGroup: w.useContext(g0),
    isPresent: t,
    safeToRemove: n,
  });
}
const hk = {
    borderRadius: {
      ...Ri,
      applyTo: [
        "borderTopLeftRadius",
        "borderTopRightRadius",
        "borderBottomLeftRadius",
        "borderBottomRightRadius",
      ],
    },
    borderTopLeftRadius: Ri,
    borderTopRightRadius: Ri,
    borderBottomLeftRadius: Ri,
    borderBottomRightRadius: Ri,
    boxShadow: ck,
  },
  v0 = ["TopLeft", "TopRight", "BottomLeft", "BottomRight"],
  pk = v0.length,
  lp = (e) => (typeof e == "string" ? parseFloat(e) : e),
  up = (e) => typeof e == "number" || V.test(e);
function mk(e, t, n, r, i, s) {
  i
    ? ((e.opacity = ae(0, n.opacity !== void 0 ? n.opacity : 1, gk(r))),
      (e.opacityExit = ae(t.opacity !== void 0 ? t.opacity : 1, 0, yk(r))))
    : s &&
      (e.opacity = ae(
        t.opacity !== void 0 ? t.opacity : 1,
        n.opacity !== void 0 ? n.opacity : 1,
        r
      ));
  for (let o = 0; o < pk; o++) {
    const a = `border${v0[o]}Radius`;
    let l = cp(t, a),
      u = cp(n, a);
    if (l === void 0 && u === void 0) continue;
    l || (l = 0),
      u || (u = 0),
      l === 0 || u === 0 || up(l) === up(u)
        ? ((e[a] = Math.max(ae(lp(l), lp(u), r), 0)),
          (Vt.test(u) || Vt.test(l)) && (e[a] += "%"))
        : (e[a] = u);
  }
  (t.rotate || n.rotate) && (e.rotate = ae(t.rotate || 0, n.rotate || 0, r));
}
function cp(e, t) {
  return e[t] !== void 0 ? e[t] : e.borderRadius;
}
const gk = x0(0, 0.5, Ev),
  yk = x0(0.5, 0.95, Ie);
function x0(e, t, n) {
  return (r) => (r < e ? 0 : r > t ? 1 : n(ci(e, t, r)));
}
function dp(e, t) {
  (e.min = t.min), (e.max = t.max);
}
function ut(e, t) {
  dp(e.x, t.x), dp(e.y, t.y);
}
function fp(e, t) {
  (e.translate = t.translate),
    (e.scale = t.scale),
    (e.originPoint = t.originPoint),
    (e.origin = t.origin);
}
function hp(e, t, n, r, i) {
  return (
    (e -= t), (e = ea(e, 1 / n, r)), i !== void 0 && (e = ea(e, 1 / i, r)), e
  );
}
function vk(e, t = 0, n = 1, r = 0.5, i, s = e, o = e) {
  if (
    (Vt.test(t) &&
      ((t = parseFloat(t)), (t = ae(o.min, o.max, t / 100) - o.min)),
    typeof t != "number")
  )
    return;
  let a = ae(s.min, s.max, r);
  e === s && (a -= t),
    (e.min = hp(e.min, t, n, a, i)),
    (e.max = hp(e.max, t, n, a, i));
}
function pp(e, t, [n, r, i], s, o) {
  vk(e, t[n], t[r], t[i], t.scale, s, o);
}
const xk = ["x", "scaleX", "originX"],
  wk = ["y", "scaleY", "originY"];
function mp(e, t, n, r) {
  pp(e.x, t, xk, n ? n.x : void 0, r ? r.x : void 0),
    pp(e.y, t, wk, n ? n.y : void 0, r ? r.y : void 0);
}
function gp(e) {
  return e.translate === 0 && e.scale === 1;
}
function w0(e) {
  return gp(e.x) && gp(e.y);
}
function yp(e, t) {
  return e.min === t.min && e.max === t.max;
}
function Sk(e, t) {
  return yp(e.x, t.x) && yp(e.y, t.y);
}
function vp(e, t) {
  return (
    Math.round(e.min) === Math.round(t.min) &&
    Math.round(e.max) === Math.round(t.max)
  );
}
function S0(e, t) {
  return vp(e.x, t.x) && vp(e.y, t.y);
}
function xp(e) {
  return it(e.x) / it(e.y);
}
function wp(e, t) {
  return (
    e.translate === t.translate &&
    e.scale === t.scale &&
    e.originPoint === t.originPoint
  );
}
class Pk {
  constructor() {
    this.members = [];
  }
  add(t) {
    xd(this.members, t), t.scheduleRender();
  }
  remove(t) {
    if (
      (wd(this.members, t),
      t === this.prevLead && (this.prevLead = void 0),
      t === this.lead)
    ) {
      const n = this.members[this.members.length - 1];
      n && this.promote(n);
    }
  }
  relegate(t) {
    const n = this.members.findIndex((i) => t === i);
    if (n === 0) return !1;
    let r;
    for (let i = n; i >= 0; i--) {
      const s = this.members[i];
      if (s.isPresent !== !1) {
        r = s;
        break;
      }
    }
    return r ? (this.promote(r), !0) : !1;
  }
  promote(t, n) {
    const r = this.lead;
    if (t !== r && ((this.prevLead = r), (this.lead = t), t.show(), r)) {
      r.instance && r.scheduleRender(),
        t.scheduleRender(),
        (t.resumeFrom = r),
        n && (t.resumeFrom.preserveOpacity = !0),
        r.snapshot &&
          ((t.snapshot = r.snapshot),
          (t.snapshot.latestValues = r.animationValues || r.latestValues)),
        t.root && t.root.isUpdating && (t.isLayoutDirty = !0);
      const { crossfade: i } = t.options;
      i === !1 && r.hide();
    }
  }
  exitAnimationComplete() {
    this.members.forEach((t) => {
      const { options: n, resumingFrom: r } = t;
      n.onExitComplete && n.onExitComplete(),
        r && r.options.onExitComplete && r.options.onExitComplete();
    });
  }
  scheduleRender() {
    this.members.forEach((t) => {
      t.instance && t.scheduleRender(!1);
    });
  }
  removeLeadSnapshot() {
    this.lead && this.lead.snapshot && (this.lead.snapshot = void 0);
  }
}
function Ck(e, t, n) {
  let r = "";
  const i = e.x.translate / t.x,
    s = e.y.translate / t.y,
    o = (n == null ? void 0 : n.z) || 0;
  if (
    ((i || s || o) && (r = `translate3d(${i}px, ${s}px, ${o}px) `),
    (t.x !== 1 || t.y !== 1) && (r += `scale(${1 / t.x}, ${1 / t.y}) `),
    n)
  ) {
    const {
      transformPerspective: u,
      rotate: c,
      rotateX: d,
      rotateY: f,
      skewX: v,
      skewY: y,
    } = n;
    u && (r = `perspective(${u}px) ${r}`),
      c && (r += `rotate(${c}deg) `),
      d && (r += `rotateX(${d}deg) `),
      f && (r += `rotateY(${f}deg) `),
      v && (r += `skewX(${v}deg) `),
      y && (r += `skewY(${y}deg) `);
  }
  const a = e.x.scale * t.x,
    l = e.y.scale * t.y;
  return (a !== 1 || l !== 1) && (r += `scale(${a}, ${l})`), r || "none";
}
const Ek = (e, t) => e.depth - t.depth;
class Tk {
  constructor() {
    (this.children = []), (this.isDirty = !1);
  }
  add(t) {
    xd(this.children, t), (this.isDirty = !0);
  }
  remove(t) {
    wd(this.children, t), (this.isDirty = !0);
  }
  forEach(t) {
    this.isDirty && this.children.sort(Ek),
      (this.isDirty = !1),
      this.children.forEach(t);
  }
}
function Co(e) {
  const t = je(e) ? e.get() : e;
  return hT(t) ? t.toValue() : t;
}
function kk(e, t) {
  const n = zt.now(),
    r = ({ timestamp: i }) => {
      const s = i - n;
      s >= t && (Bn(r), e(s - t));
    };
  return Y.read(r, !0), () => Bn(r);
}
function Ak(e) {
  return e instanceof SVGElement && e.tagName !== "svg";
}
function Rk(e, t, n) {
  const r = je(e) ? e : xs(e);
  return r.start(vd("", r, t, n)), r.animation;
}
const Zn = {
    type: "projectionFrame",
    totalNodes: 0,
    resolvedTargetDeltas: 0,
    recalculatedProjection: 0,
  },
  Oi = typeof window < "u" && window.MotionDebug !== void 0,
  Rl = ["", "X", "Y", "Z"],
  Mk = { visibility: "hidden" },
  Sp = 1e3;
let Dk = 0;
function Ml(e, t, n, r) {
  const { latestValues: i } = t;
  i[e] && ((n[e] = i[e]), t.setStaticValue(e, 0), r && (r[e] = 0));
}
function P0(e) {
  if (((e.hasCheckedOptimisedAppear = !0), e.root === e)) return;
  const { visualElement: t } = e.options;
  if (!t) return;
  const n = t0(t);
  if (window.MotionHasOptimisedAnimation(n, "transform")) {
    const { layout: i, layoutId: s } = e.options;
    window.MotionCancelOptimisedAnimation(n, "transform", Y, !(i || s));
  }
  const { parent: r } = e;
  r && !r.hasCheckedOptimisedAppear && P0(r);
}
function C0({
  attachResizeListener: e,
  defaultParent: t,
  measureScroll: n,
  checkIsScrollRoot: r,
  resetTransform: i,
}) {
  return class {
    constructor(o = {}, a = t == null ? void 0 : t()) {
      (this.id = Dk++),
        (this.animationId = 0),
        (this.children = new Set()),
        (this.options = {}),
        (this.isTreeAnimating = !1),
        (this.isAnimationBlocked = !1),
        (this.isLayoutDirty = !1),
        (this.isProjectionDirty = !1),
        (this.isSharedProjectionDirty = !1),
        (this.isTransformDirty = !1),
        (this.updateManuallyBlocked = !1),
        (this.updateBlockedByResize = !1),
        (this.isUpdating = !1),
        (this.isSVG = !1),
        (this.needsReset = !1),
        (this.shouldResetTransform = !1),
        (this.hasCheckedOptimisedAppear = !1),
        (this.treeScale = { x: 1, y: 1 }),
        (this.eventHandlers = new Map()),
        (this.hasTreeAnimated = !1),
        (this.updateScheduled = !1),
        (this.scheduleUpdate = () => this.update()),
        (this.projectionUpdateScheduled = !1),
        (this.checkUpdateFailed = () => {
          this.isUpdating && ((this.isUpdating = !1), this.clearAllSnapshots());
        }),
        (this.updateProjection = () => {
          (this.projectionUpdateScheduled = !1),
            Oi &&
              (Zn.totalNodes =
                Zn.resolvedTargetDeltas =
                Zn.recalculatedProjection =
                  0),
            this.nodes.forEach(Lk),
            this.nodes.forEach(_k),
            this.nodes.forEach(Vk),
            this.nodes.forEach(Ok),
            Oi && window.MotionDebug.record(Zn);
        }),
        (this.resolvedRelativeTargetAt = 0),
        (this.hasProjected = !1),
        (this.isVisible = !0),
        (this.animationProgress = 0),
        (this.sharedNodes = new Map()),
        (this.latestValues = o),
        (this.root = a ? a.root || a : this),
        (this.path = a ? [...a.path, a] : []),
        (this.parent = a),
        (this.depth = a ? a.depth + 1 : 0);
      for (let l = 0; l < this.path.length; l++)
        this.path[l].shouldResetTransform = !0;
      this.root === this && (this.nodes = new Tk());
    }
    addEventListener(o, a) {
      return (
        this.eventHandlers.has(o) || this.eventHandlers.set(o, new Sd()),
        this.eventHandlers.get(o).add(a)
      );
    }
    notifyListeners(o, ...a) {
      const l = this.eventHandlers.get(o);
      l && l.notify(...a);
    }
    hasListeners(o) {
      return this.eventHandlers.has(o);
    }
    mount(o, a = this.root.hasTreeAnimated) {
      if (this.instance) return;
      (this.isSVG = Ak(o)), (this.instance = o);
      const { layoutId: l, layout: u, visualElement: c } = this.options;
      if (
        (c && !c.current && c.mount(o),
        this.root.nodes.add(this),
        this.parent && this.parent.children.add(this),
        a && (u || l) && (this.isLayoutDirty = !0),
        e)
      ) {
        let d;
        const f = () => (this.root.updateBlockedByResize = !1);
        e(o, () => {
          (this.root.updateBlockedByResize = !0),
            d && d(),
            (d = kk(f, 250)),
            Po.hasAnimatedSinceResize &&
              ((Po.hasAnimatedSinceResize = !1), this.nodes.forEach(Cp));
        });
      }
      l && this.root.registerSharedNode(l, this),
        this.options.animate !== !1 &&
          c &&
          (l || u) &&
          this.addEventListener(
            "didUpdate",
            ({
              delta: d,
              hasLayoutChanged: f,
              hasRelativeTargetChanged: v,
              layout: y,
            }) => {
              if (this.isTreeAnimationBlocked()) {
                (this.target = void 0), (this.relativeTarget = void 0);
                return;
              }
              const m =
                  this.options.transition || c.getDefaultTransition() || Wk,
                { onLayoutAnimationStart: x, onLayoutAnimationComplete: h } =
                  c.getProps(),
                p = !this.targetLayout || !S0(this.targetLayout, y) || v,
                g = !f && v;
              if (
                this.options.layoutRoot ||
                (this.resumeFrom && this.resumeFrom.instance) ||
                g ||
                (f && (p || !this.currentAnimation))
              ) {
                this.resumeFrom &&
                  ((this.resumingFrom = this.resumeFrom),
                  (this.resumingFrom.resumingFrom = void 0)),
                  this.setAnimationOrigin(d, g);
                const S = { ...id(m, "layout"), onPlay: x, onComplete: h };
                (c.shouldReduceMotion || this.options.layoutRoot) &&
                  ((S.delay = 0), (S.type = !1)),
                  this.startAnimation(S);
              } else
                f || Cp(this),
                  this.isLead() &&
                    this.options.onExitComplete &&
                    this.options.onExitComplete();
              this.targetLayout = y;
            }
          );
    }
    unmount() {
      this.options.layoutId && this.willUpdate(), this.root.nodes.remove(this);
      const o = this.getStack();
      o && o.remove(this),
        this.parent && this.parent.children.delete(this),
        (this.instance = void 0),
        Bn(this.updateProjection);
    }
    blockUpdate() {
      this.updateManuallyBlocked = !0;
    }
    unblockUpdate() {
      this.updateManuallyBlocked = !1;
    }
    isUpdateBlocked() {
      return this.updateManuallyBlocked || this.updateBlockedByResize;
    }
    isTreeAnimationBlocked() {
      return (
        this.isAnimationBlocked ||
        (this.parent && this.parent.isTreeAnimationBlocked()) ||
        !1
      );
    }
    startUpdate() {
      this.isUpdateBlocked() ||
        ((this.isUpdating = !0),
        this.nodes && this.nodes.forEach(zk),
        this.animationId++);
    }
    getTransformTemplate() {
      const { visualElement: o } = this.options;
      return o && o.getProps().transformTemplate;
    }
    willUpdate(o = !0) {
      if (((this.root.hasTreeAnimated = !0), this.root.isUpdateBlocked())) {
        this.options.onExitComplete && this.options.onExitComplete();
        return;
      }
      if (
        (window.MotionCancelOptimisedAnimation &&
          !this.hasCheckedOptimisedAppear &&
          P0(this),
        !this.root.isUpdating && this.root.startUpdate(),
        this.isLayoutDirty)
      )
        return;
      this.isLayoutDirty = !0;
      for (let c = 0; c < this.path.length; c++) {
        const d = this.path[c];
        (d.shouldResetTransform = !0),
          d.updateScroll("snapshot"),
          d.options.layoutRoot && d.willUpdate(!1);
      }
      const { layoutId: a, layout: l } = this.options;
      if (a === void 0 && !l) return;
      const u = this.getTransformTemplate();
      (this.prevTransformTemplateValue = u ? u(this.latestValues, "") : void 0),
        this.updateSnapshot(),
        o && this.notifyListeners("willUpdate");
    }
    update() {
      if (((this.updateScheduled = !1), this.isUpdateBlocked())) {
        this.unblockUpdate(), this.clearAllSnapshots(), this.nodes.forEach(Pp);
        return;
      }
      this.isUpdating || this.nodes.forEach(Ik),
        (this.isUpdating = !1),
        this.nodes.forEach(Fk),
        this.nodes.forEach(Nk),
        this.nodes.forEach(bk),
        this.clearAllSnapshots();
      const a = zt.now();
      (ke.delta = an(0, 1e3 / 60, a - ke.timestamp)),
        (ke.timestamp = a),
        (ke.isProcessing = !0),
        wl.update.process(ke),
        wl.preRender.process(ke),
        wl.render.process(ke),
        (ke.isProcessing = !1);
    }
    didUpdate() {
      this.updateScheduled ||
        ((this.updateScheduled = !0), Ed.read(this.scheduleUpdate));
    }
    clearAllSnapshots() {
      this.nodes.forEach(jk), this.sharedNodes.forEach(Bk);
    }
    scheduleUpdateProjection() {
      this.projectionUpdateScheduled ||
        ((this.projectionUpdateScheduled = !0),
        Y.preRender(this.updateProjection, !1, !0));
    }
    scheduleCheckAfterUnmount() {
      Y.postRender(() => {
        this.isLayoutDirty
          ? this.root.didUpdate()
          : this.root.checkUpdateFailed();
      });
    }
    updateSnapshot() {
      this.snapshot || !this.instance || (this.snapshot = this.measure());
    }
    updateLayout() {
      if (
        !this.instance ||
        (this.updateScroll(),
        !(this.options.alwaysMeasureLayout && this.isLead()) &&
          !this.isLayoutDirty)
      )
        return;
      if (this.resumeFrom && !this.resumeFrom.instance)
        for (let l = 0; l < this.path.length; l++) this.path[l].updateScroll();
      const o = this.layout;
      (this.layout = this.measure(!1)),
        (this.layoutCorrected = pe()),
        (this.isLayoutDirty = !1),
        (this.projectionDelta = void 0),
        this.notifyListeners("measure", this.layout.layoutBox);
      const { visualElement: a } = this.options;
      a &&
        a.notify(
          "LayoutMeasure",
          this.layout.layoutBox,
          o ? o.layoutBox : void 0
        );
    }
    updateScroll(o = "measure") {
      let a = !!(this.options.layoutScroll && this.instance);
      if (
        (this.scroll &&
          this.scroll.animationId === this.root.animationId &&
          this.scroll.phase === o &&
          (a = !1),
        a)
      ) {
        const l = r(this.instance);
        this.scroll = {
          animationId: this.root.animationId,
          phase: o,
          isRoot: l,
          offset: n(this.instance),
          wasRoot: this.scroll ? this.scroll.isRoot : l,
        };
      }
    }
    resetTransform() {
      if (!i) return;
      const o =
          this.isLayoutDirty ||
          this.shouldResetTransform ||
          this.options.alwaysMeasureLayout,
        a = this.projectionDelta && !w0(this.projectionDelta),
        l = this.getTransformTemplate(),
        u = l ? l(this.latestValues, "") : void 0,
        c = u !== this.prevTransformTemplateValue;
      o &&
        (a || Yn(this.latestValues) || c) &&
        (i(this.instance, u),
        (this.shouldResetTransform = !1),
        this.scheduleRender());
    }
    measure(o = !0) {
      const a = this.measurePageBox();
      let l = this.removeElementScroll(a);
      return (
        o && (l = this.removeTransform(l)),
        Hk(l),
        {
          animationId: this.root.animationId,
          measuredBox: a,
          layoutBox: l,
          latestValues: {},
          source: this.id,
        }
      );
    }
    measurePageBox() {
      var o;
      const { visualElement: a } = this.options;
      if (!a) return pe();
      const l = a.measureViewportBox();
      if (
        !(
          ((o = this.scroll) === null || o === void 0 ? void 0 : o.wasRoot) ||
          this.path.some(Kk)
        )
      ) {
        const { scroll: c } = this.root;
        c && (Fr(l.x, c.offset.x), Fr(l.y, c.offset.y));
      }
      return l;
    }
    removeElementScroll(o) {
      var a;
      const l = pe();
      if (
        (ut(l, o), !((a = this.scroll) === null || a === void 0) && a.wasRoot)
      )
        return l;
      for (let u = 0; u < this.path.length; u++) {
        const c = this.path[u],
          { scroll: d, options: f } = c;
        c !== this.root &&
          d &&
          f.layoutScroll &&
          (d.wasRoot && ut(l, o), Fr(l.x, d.offset.x), Fr(l.y, d.offset.y));
      }
      return l;
    }
    applyTransform(o, a = !1) {
      const l = pe();
      ut(l, o);
      for (let u = 0; u < this.path.length; u++) {
        const c = this.path[u];
        !a &&
          c.options.layoutScroll &&
          c.scroll &&
          c !== c.root &&
          _r(l, { x: -c.scroll.offset.x, y: -c.scroll.offset.y }),
          Yn(c.latestValues) && _r(l, c.latestValues);
      }
      return Yn(this.latestValues) && _r(l, this.latestValues), l;
    }
    removeTransform(o) {
      const a = pe();
      ut(a, o);
      for (let l = 0; l < this.path.length; l++) {
        const u = this.path[l];
        if (!u.instance || !Yn(u.latestValues)) continue;
        Hu(u.latestValues) && u.updateSnapshot();
        const c = pe(),
          d = u.measurePageBox();
        ut(c, d),
          mp(a, u.latestValues, u.snapshot ? u.snapshot.layoutBox : void 0, c);
      }
      return Yn(this.latestValues) && mp(a, this.latestValues), a;
    }
    setTargetDelta(o) {
      (this.targetDelta = o),
        this.root.scheduleUpdateProjection(),
        (this.isProjectionDirty = !0);
    }
    setOptions(o) {
      this.options = {
        ...this.options,
        ...o,
        crossfade: o.crossfade !== void 0 ? o.crossfade : !0,
      };
    }
    clearMeasurements() {
      (this.scroll = void 0),
        (this.layout = void 0),
        (this.snapshot = void 0),
        (this.prevTransformTemplateValue = void 0),
        (this.targetDelta = void 0),
        (this.target = void 0),
        (this.isLayoutDirty = !1);
    }
    forceRelativeParentToResolveTarget() {
      this.relativeParent &&
        this.relativeParent.resolvedRelativeTargetAt !== ke.timestamp &&
        this.relativeParent.resolveTargetDelta(!0);
    }
    resolveTargetDelta(o = !1) {
      var a;
      const l = this.getLead();
      this.isProjectionDirty || (this.isProjectionDirty = l.isProjectionDirty),
        this.isTransformDirty || (this.isTransformDirty = l.isTransformDirty),
        this.isSharedProjectionDirty ||
          (this.isSharedProjectionDirty = l.isSharedProjectionDirty);
      const u = !!this.resumingFrom || this !== l;
      if (
        !(
          o ||
          (u && this.isSharedProjectionDirty) ||
          this.isProjectionDirty ||
          (!((a = this.parent) === null || a === void 0) &&
            a.isProjectionDirty) ||
          this.attemptToResolveRelativeTarget ||
          this.root.updateBlockedByResize
        )
      )
        return;
      const { layout: d, layoutId: f } = this.options;
      if (!(!this.layout || !(d || f))) {
        if (
          ((this.resolvedRelativeTargetAt = ke.timestamp),
          !this.targetDelta && !this.relativeTarget)
        ) {
          const v = this.getClosestProjectingParent();
          v && v.layout && this.animationProgress !== 1
            ? ((this.relativeParent = v),
              this.forceRelativeParentToResolveTarget(),
              (this.relativeTarget = pe()),
              (this.relativeTargetOrigin = pe()),
              Gi(
                this.relativeTargetOrigin,
                this.layout.layoutBox,
                v.layout.layoutBox
              ),
              ut(this.relativeTarget, this.relativeTargetOrigin))
            : (this.relativeParent = this.relativeTarget = void 0);
        }
        if (!(!this.relativeTarget && !this.targetDelta)) {
          if (
            (this.target ||
              ((this.target = pe()), (this.targetWithTransforms = pe())),
            this.relativeTarget &&
            this.relativeTargetOrigin &&
            this.relativeParent &&
            this.relativeParent.target
              ? (this.forceRelativeParentToResolveTarget(),
                QT(
                  this.target,
                  this.relativeTarget,
                  this.relativeParent.target
                ))
              : this.targetDelta
              ? (this.resumingFrom
                  ? (this.target = this.applyTransform(this.layout.layoutBox))
                  : ut(this.target, this.layout.layoutBox),
                f0(this.target, this.targetDelta))
              : ut(this.target, this.layout.layoutBox),
            this.attemptToResolveRelativeTarget)
          ) {
            this.attemptToResolveRelativeTarget = !1;
            const v = this.getClosestProjectingParent();
            v &&
            !!v.resumingFrom == !!this.resumingFrom &&
            !v.options.layoutScroll &&
            v.target &&
            this.animationProgress !== 1
              ? ((this.relativeParent = v),
                this.forceRelativeParentToResolveTarget(),
                (this.relativeTarget = pe()),
                (this.relativeTargetOrigin = pe()),
                Gi(this.relativeTargetOrigin, this.target, v.target),
                ut(this.relativeTarget, this.relativeTargetOrigin))
              : (this.relativeParent = this.relativeTarget = void 0);
          }
          Oi && Zn.resolvedTargetDeltas++;
        }
      }
    }
    getClosestProjectingParent() {
      if (
        !(
          !this.parent ||
          Hu(this.parent.latestValues) ||
          d0(this.parent.latestValues)
        )
      )
        return this.parent.isProjecting()
          ? this.parent
          : this.parent.getClosestProjectingParent();
    }
    isProjecting() {
      return !!(
        (this.relativeTarget || this.targetDelta || this.options.layoutRoot) &&
        this.layout
      );
    }
    calcProjection() {
      var o;
      const a = this.getLead(),
        l = !!this.resumingFrom || this !== a;
      let u = !0;
      if (
        ((this.isProjectionDirty ||
          (!((o = this.parent) === null || o === void 0) &&
            o.isProjectionDirty)) &&
          (u = !1),
        l &&
          (this.isSharedProjectionDirty || this.isTransformDirty) &&
          (u = !1),
        this.resolvedRelativeTargetAt === ke.timestamp && (u = !1),
        u)
      )
        return;
      const { layout: c, layoutId: d } = this.options;
      if (
        ((this.isTreeAnimating = !!(
          (this.parent && this.parent.isTreeAnimating) ||
          this.currentAnimation ||
          this.pendingAnimation
        )),
        this.isTreeAnimating ||
          (this.targetDelta = this.relativeTarget = void 0),
        !this.layout || !(c || d))
      )
        return;
      ut(this.layoutCorrected, this.layout.layoutBox);
      const f = this.treeScale.x,
        v = this.treeScale.y;
      nk(this.layoutCorrected, this.treeScale, this.path, l),
        a.layout &&
          !a.target &&
          (this.treeScale.x !== 1 || this.treeScale.y !== 1) &&
          ((a.target = a.layout.layoutBox), (a.targetWithTransforms = pe()));
      const { target: y } = a;
      if (!y) {
        this.prevProjectionDelta &&
          (this.createProjectionDeltas(), this.scheduleRender());
        return;
      }
      !this.projectionDelta || !this.prevProjectionDelta
        ? this.createProjectionDeltas()
        : (fp(this.prevProjectionDelta.x, this.projectionDelta.x),
          fp(this.prevProjectionDelta.y, this.projectionDelta.y)),
        Qi(this.projectionDelta, this.layoutCorrected, y, this.latestValues),
        (this.treeScale.x !== f ||
          this.treeScale.y !== v ||
          !wp(this.projectionDelta.x, this.prevProjectionDelta.x) ||
          !wp(this.projectionDelta.y, this.prevProjectionDelta.y)) &&
          ((this.hasProjected = !0),
          this.scheduleRender(),
          this.notifyListeners("projectionUpdate", y)),
        Oi && Zn.recalculatedProjection++;
    }
    hide() {
      this.isVisible = !1;
    }
    show() {
      this.isVisible = !0;
    }
    scheduleRender(o = !0) {
      var a;
      if (
        ((a = this.options.visualElement) === null ||
          a === void 0 ||
          a.scheduleRender(),
        o)
      ) {
        const l = this.getStack();
        l && l.scheduleRender();
      }
      this.resumingFrom &&
        !this.resumingFrom.instance &&
        (this.resumingFrom = void 0);
    }
    createProjectionDeltas() {
      (this.prevProjectionDelta = Ir()),
        (this.projectionDelta = Ir()),
        (this.projectionDeltaWithTransform = Ir());
    }
    setAnimationOrigin(o, a = !1) {
      const l = this.snapshot,
        u = l ? l.latestValues : {},
        c = { ...this.latestValues },
        d = Ir();
      (!this.relativeParent || !this.relativeParent.options.layoutRoot) &&
        (this.relativeTarget = this.relativeTargetOrigin = void 0),
        (this.attemptToResolveRelativeTarget = !a);
      const f = pe(),
        v = l ? l.source : void 0,
        y = this.layout ? this.layout.source : void 0,
        m = v !== y,
        x = this.getStack(),
        h = !x || x.members.length <= 1,
        p = !!(m && !h && this.options.crossfade === !0 && !this.path.some($k));
      this.animationProgress = 0;
      let g;
      (this.mixTargetDelta = (S) => {
        const C = S / 1e3;
        Ep(d.x, o.x, C),
          Ep(d.y, o.y, C),
          this.setTargetDelta(d),
          this.relativeTarget &&
            this.relativeTargetOrigin &&
            this.layout &&
            this.relativeParent &&
            this.relativeParent.layout &&
            (Gi(f, this.layout.layoutBox, this.relativeParent.layout.layoutBox),
            Uk(this.relativeTarget, this.relativeTargetOrigin, f, C),
            g && Sk(this.relativeTarget, g) && (this.isProjectionDirty = !1),
            g || (g = pe()),
            ut(g, this.relativeTarget)),
          m &&
            ((this.animationValues = c), mk(c, u, this.latestValues, C, p, h)),
          this.root.scheduleUpdateProjection(),
          this.scheduleRender(),
          (this.animationProgress = C);
      }),
        this.mixTargetDelta(this.options.layoutRoot ? 1e3 : 0);
    }
    startAnimation(o) {
      this.notifyListeners("animationStart"),
        this.currentAnimation && this.currentAnimation.stop(),
        this.resumingFrom &&
          this.resumingFrom.currentAnimation &&
          this.resumingFrom.currentAnimation.stop(),
        this.pendingAnimation &&
          (Bn(this.pendingAnimation), (this.pendingAnimation = void 0)),
        (this.pendingAnimation = Y.update(() => {
          (Po.hasAnimatedSinceResize = !0),
            (this.currentAnimation = Rk(0, Sp, {
              ...o,
              onUpdate: (a) => {
                this.mixTargetDelta(a), o.onUpdate && o.onUpdate(a);
              },
              onComplete: () => {
                o.onComplete && o.onComplete(), this.completeAnimation();
              },
            })),
            this.resumingFrom &&
              (this.resumingFrom.currentAnimation = this.currentAnimation),
            (this.pendingAnimation = void 0);
        }));
    }
    completeAnimation() {
      this.resumingFrom &&
        ((this.resumingFrom.currentAnimation = void 0),
        (this.resumingFrom.preserveOpacity = void 0));
      const o = this.getStack();
      o && o.exitAnimationComplete(),
        (this.resumingFrom =
          this.currentAnimation =
          this.animationValues =
            void 0),
        this.notifyListeners("animationComplete");
    }
    finishAnimation() {
      this.currentAnimation &&
        (this.mixTargetDelta && this.mixTargetDelta(Sp),
        this.currentAnimation.stop()),
        this.completeAnimation();
    }
    applyTransformsToTarget() {
      const o = this.getLead();
      let {
        targetWithTransforms: a,
        target: l,
        layout: u,
        latestValues: c,
      } = o;
      if (!(!a || !l || !u)) {
        if (
          this !== o &&
          this.layout &&
          u &&
          E0(this.options.animationType, this.layout.layoutBox, u.layoutBox)
        ) {
          l = this.target || pe();
          const d = it(this.layout.layoutBox.x);
          (l.x.min = o.target.x.min), (l.x.max = l.x.min + d);
          const f = it(this.layout.layoutBox.y);
          (l.y.min = o.target.y.min), (l.y.max = l.y.min + f);
        }
        ut(a, l),
          _r(a, c),
          Qi(this.projectionDeltaWithTransform, this.layoutCorrected, a, c);
      }
    }
    registerSharedNode(o, a) {
      this.sharedNodes.has(o) || this.sharedNodes.set(o, new Pk()),
        this.sharedNodes.get(o).add(a);
      const u = a.options.initialPromotionConfig;
      a.promote({
        transition: u ? u.transition : void 0,
        preserveFollowOpacity:
          u && u.shouldPreserveFollowOpacity
            ? u.shouldPreserveFollowOpacity(a)
            : void 0,
      });
    }
    isLead() {
      const o = this.getStack();
      return o ? o.lead === this : !0;
    }
    getLead() {
      var o;
      const { layoutId: a } = this.options;
      return a
        ? ((o = this.getStack()) === null || o === void 0 ? void 0 : o.lead) ||
            this
        : this;
    }
    getPrevLead() {
      var o;
      const { layoutId: a } = this.options;
      return a
        ? (o = this.getStack()) === null || o === void 0
          ? void 0
          : o.prevLead
        : void 0;
    }
    getStack() {
      const { layoutId: o } = this.options;
      if (o) return this.root.sharedNodes.get(o);
    }
    promote({ needsReset: o, transition: a, preserveFollowOpacity: l } = {}) {
      const u = this.getStack();
      u && u.promote(this, l),
        o && ((this.projectionDelta = void 0), (this.needsReset = !0)),
        a && this.setOptions({ transition: a });
    }
    relegate() {
      const o = this.getStack();
      return o ? o.relegate(this) : !1;
    }
    resetSkewAndRotation() {
      const { visualElement: o } = this.options;
      if (!o) return;
      let a = !1;
      const { latestValues: l } = o;
      if (
        ((l.z ||
          l.rotate ||
          l.rotateX ||
          l.rotateY ||
          l.rotateZ ||
          l.skewX ||
          l.skewY) &&
          (a = !0),
        !a)
      )
        return;
      const u = {};
      l.z && Ml("z", o, u, this.animationValues);
      for (let c = 0; c < Rl.length; c++)
        Ml(`rotate${Rl[c]}`, o, u, this.animationValues),
          Ml(`skew${Rl[c]}`, o, u, this.animationValues);
      o.render();
      for (const c in u)
        o.setStaticValue(c, u[c]),
          this.animationValues && (this.animationValues[c] = u[c]);
      o.scheduleRender();
    }
    getProjectionStyles(o) {
      var a, l;
      if (!this.instance || this.isSVG) return;
      if (!this.isVisible) return Mk;
      const u = { visibility: "" },
        c = this.getTransformTemplate();
      if (this.needsReset)
        return (
          (this.needsReset = !1),
          (u.opacity = ""),
          (u.pointerEvents = Co(o == null ? void 0 : o.pointerEvents) || ""),
          (u.transform = c ? c(this.latestValues, "") : "none"),
          u
        );
      const d = this.getLead();
      if (!this.projectionDelta || !this.layout || !d.target) {
        const m = {};
        return (
          this.options.layoutId &&
            ((m.opacity =
              this.latestValues.opacity !== void 0
                ? this.latestValues.opacity
                : 1),
            (m.pointerEvents = Co(o == null ? void 0 : o.pointerEvents) || "")),
          this.hasProjected &&
            !Yn(this.latestValues) &&
            ((m.transform = c ? c({}, "") : "none"), (this.hasProjected = !1)),
          m
        );
      }
      const f = d.animationValues || d.latestValues;
      this.applyTransformsToTarget(),
        (u.transform = Ck(
          this.projectionDeltaWithTransform,
          this.treeScale,
          f
        )),
        c && (u.transform = c(f, u.transform));
      const { x: v, y } = this.projectionDelta;
      (u.transformOrigin = `${v.origin * 100}% ${y.origin * 100}% 0`),
        d.animationValues
          ? (u.opacity =
              d === this
                ? (l =
                    (a = f.opacity) !== null && a !== void 0
                      ? a
                      : this.latestValues.opacity) !== null && l !== void 0
                  ? l
                  : 1
                : this.preserveOpacity
                ? this.latestValues.opacity
                : f.opacityExit)
          : (u.opacity =
              d === this
                ? f.opacity !== void 0
                  ? f.opacity
                  : ""
                : f.opacityExit !== void 0
                ? f.opacityExit
                : 0);
      for (const m in ta) {
        if (f[m] === void 0) continue;
        const { correct: x, applyTo: h } = ta[m],
          p = u.transform === "none" ? f[m] : x(f[m], d);
        if (h) {
          const g = h.length;
          for (let S = 0; S < g; S++) u[h[S]] = p;
        } else u[m] = p;
      }
      return (
        this.options.layoutId &&
          (u.pointerEvents =
            d === this
              ? Co(o == null ? void 0 : o.pointerEvents) || ""
              : "none"),
        u
      );
    }
    clearSnapshot() {
      this.resumeFrom = this.snapshot = void 0;
    }
    resetTree() {
      this.root.nodes.forEach((o) => {
        var a;
        return (a = o.currentAnimation) === null || a === void 0
          ? void 0
          : a.stop();
      }),
        this.root.nodes.forEach(Pp),
        this.root.sharedNodes.clear();
    }
  };
}
function Nk(e) {
  e.updateLayout();
}
function bk(e) {
  var t;
  const n =
    ((t = e.resumeFrom) === null || t === void 0 ? void 0 : t.snapshot) ||
    e.snapshot;
  if (e.isLead() && e.layout && n && e.hasListeners("didUpdate")) {
    const { layoutBox: r, measuredBox: i } = e.layout,
      { animationType: s } = e.options,
      o = n.source !== e.layout.source;
    s === "size"
      ? ct((d) => {
          const f = o ? n.measuredBox[d] : n.layoutBox[d],
            v = it(f);
          (f.min = r[d].min), (f.max = f.min + v);
        })
      : E0(s, n.layoutBox, r) &&
        ct((d) => {
          const f = o ? n.measuredBox[d] : n.layoutBox[d],
            v = it(r[d]);
          (f.max = f.min + v),
            e.relativeTarget &&
              !e.currentAnimation &&
              ((e.isProjectionDirty = !0),
              (e.relativeTarget[d].max = e.relativeTarget[d].min + v));
        });
    const a = Ir();
    Qi(a, r, n.layoutBox);
    const l = Ir();
    o ? Qi(l, e.applyTransform(i, !0), n.measuredBox) : Qi(l, r, n.layoutBox);
    const u = !w0(a);
    let c = !1;
    if (!e.resumeFrom) {
      const d = e.getClosestProjectingParent();
      if (d && !d.resumeFrom) {
        const { snapshot: f, layout: v } = d;
        if (f && v) {
          const y = pe();
          Gi(y, n.layoutBox, f.layoutBox);
          const m = pe();
          Gi(m, r, v.layoutBox),
            S0(y, m) || (c = !0),
            d.options.layoutRoot &&
              ((e.relativeTarget = m),
              (e.relativeTargetOrigin = y),
              (e.relativeParent = d));
        }
      }
    }
    e.notifyListeners("didUpdate", {
      layout: r,
      snapshot: n,
      delta: l,
      layoutDelta: a,
      hasLayoutChanged: u,
      hasRelativeTargetChanged: c,
    });
  } else if (e.isLead()) {
    const { onExitComplete: r } = e.options;
    r && r();
  }
  e.options.transition = void 0;
}
function Lk(e) {
  Oi && Zn.totalNodes++,
    e.parent &&
      (e.isProjecting() || (e.isProjectionDirty = e.parent.isProjectionDirty),
      e.isSharedProjectionDirty ||
        (e.isSharedProjectionDirty = !!(
          e.isProjectionDirty ||
          e.parent.isProjectionDirty ||
          e.parent.isSharedProjectionDirty
        )),
      e.isTransformDirty || (e.isTransformDirty = e.parent.isTransformDirty));
}
function Ok(e) {
  e.isProjectionDirty = e.isSharedProjectionDirty = e.isTransformDirty = !1;
}
function jk(e) {
  e.clearSnapshot();
}
function Pp(e) {
  e.clearMeasurements();
}
function Ik(e) {
  e.isLayoutDirty = !1;
}
function Fk(e) {
  const { visualElement: t } = e.options;
  t && t.getProps().onBeforeLayoutMeasure && t.notify("BeforeLayoutMeasure"),
    e.resetTransform();
}
function Cp(e) {
  e.finishAnimation(),
    (e.targetDelta = e.relativeTarget = e.target = void 0),
    (e.isProjectionDirty = !0);
}
function _k(e) {
  e.resolveTargetDelta();
}
function Vk(e) {
  e.calcProjection();
}
function zk(e) {
  e.resetSkewAndRotation();
}
function Bk(e) {
  e.removeLeadSnapshot();
}
function Ep(e, t, n) {
  (e.translate = ae(t.translate, 0, n)),
    (e.scale = ae(t.scale, 1, n)),
    (e.origin = t.origin),
    (e.originPoint = t.originPoint);
}
function Tp(e, t, n, r) {
  (e.min = ae(t.min, n.min, r)), (e.max = ae(t.max, n.max, r));
}
function Uk(e, t, n, r) {
  Tp(e.x, t.x, n.x, r), Tp(e.y, t.y, n.y, r);
}
function $k(e) {
  return e.animationValues && e.animationValues.opacityExit !== void 0;
}
const Wk = { duration: 0.45, ease: [0.4, 0, 0.1, 1] },
  kp = (e) =>
    typeof navigator < "u" &&
    navigator.userAgent &&
    navigator.userAgent.toLowerCase().includes(e),
  Ap = kp("applewebkit/") && !kp("chrome/") ? Math.round : Ie;
function Rp(e) {
  (e.min = Ap(e.min)), (e.max = Ap(e.max));
}
function Hk(e) {
  Rp(e.x), Rp(e.y);
}
function E0(e, t, n) {
  return (
    e === "position" || (e === "preserve-aspect" && !KT(xp(t), xp(n), 0.2))
  );
}
function Kk(e) {
  var t;
  return (
    e !== e.root &&
    ((t = e.scroll) === null || t === void 0 ? void 0 : t.wasRoot)
  );
}
const Qk = C0({
    attachResizeListener: (e, t) => Yt(e, "resize", t),
    measureScroll: () => ({
      x: document.documentElement.scrollLeft || document.body.scrollLeft,
      y: document.documentElement.scrollTop || document.body.scrollTop,
    }),
    checkIsScrollRoot: () => !0,
  }),
  Dl = { current: void 0 },
  T0 = C0({
    measureScroll: (e) => ({ x: e.scrollLeft, y: e.scrollTop }),
    defaultParent: () => {
      if (!Dl.current) {
        const e = new Qk({});
        e.mount(window), e.setOptions({ layoutScroll: !0 }), (Dl.current = e);
      }
      return Dl.current;
    },
    resetTransform: (e, t) => {
      e.style.transform = t !== void 0 ? t : "none";
    },
    checkIsScrollRoot: (e) => window.getComputedStyle(e).position === "fixed",
  }),
  Gk = {
    pan: { Feature: lk },
    drag: { Feature: ak, ProjectionNode: T0, MeasureLayout: y0 },
  };
function Mp(e, t, n) {
  const { props: r } = e;
  e.animationState &&
    r.whileHover &&
    e.animationState.setActive("whileHover", n);
  const i = r[n ? "onHoverStart" : "onHoverEnd"];
  i && Y.postRender(() => i(t, Ls(t)));
}
class qk extends Kn {
  mount() {
    const { current: t, props: n } = this.node;
    t &&
      (this.unmount = IT(
        t,
        (r) => (Mp(this.node, r, !0), (i) => Mp(this.node, i, !1)),
        { passive: !n.onHoverStart && !n.onHoverEnd }
      ));
  }
  unmount() {}
}
class Xk extends Kn {
  constructor() {
    super(...arguments), (this.isActive = !1);
  }
  onFocus() {
    let t = !1;
    try {
      t = this.node.current.matches(":focus-visible");
    } catch {
      t = !0;
    }
    !t ||
      !this.node.animationState ||
      (this.node.animationState.setActive("whileFocus", !0),
      (this.isActive = !0));
  }
  onBlur() {
    !this.isActive ||
      !this.node.animationState ||
      (this.node.animationState.setActive("whileFocus", !1),
      (this.isActive = !1));
  }
  mount() {
    this.unmount = Fn(
      Yt(this.node.current, "focus", () => this.onFocus()),
      Yt(this.node.current, "blur", () => this.onBlur())
    );
  }
  unmount() {}
}
const k0 = (e, t) => (t ? (e === t ? !0 : k0(e, t.parentElement)) : !1);
function Nl(e, t) {
  if (!t) return;
  const n = new PointerEvent("pointer" + e);
  t(n, Ls(n));
}
class Yk extends Kn {
  constructor() {
    super(...arguments),
      (this.removeStartListeners = Ie),
      (this.removeEndListeners = Ie),
      (this.removeAccessibleListeners = Ie),
      (this.startPointerPress = (t, n) => {
        if (this.isPressing) return;
        this.removeEndListeners();
        const r = this.node.getProps(),
          s = _n(
            window,
            "pointerup",
            (a, l) => {
              if (!this.checkPressEnd()) return;
              const {
                  onTap: u,
                  onTapCancel: c,
                  globalTapTarget: d,
                } = this.node.getProps(),
                f = !d && !k0(this.node.current, a.target) ? c : u;
              f && Y.update(() => f(a, l));
            },
            { passive: !(r.onTap || r.onPointerUp) }
          ),
          o = _n(window, "pointercancel", (a, l) => this.cancelPress(a, l), {
            passive: !(r.onTapCancel || r.onPointerCancel),
          });
        (this.removeEndListeners = Fn(s, o)), this.startPress(t, n);
      }),
      (this.startAccessiblePress = () => {
        const t = (s) => {
            if (s.key !== "Enter" || this.isPressing) return;
            const o = (a) => {
              a.key !== "Enter" ||
                !this.checkPressEnd() ||
                Nl("up", (l, u) => {
                  const { onTap: c } = this.node.getProps();
                  c && Y.postRender(() => c(l, u));
                });
            };
            this.removeEndListeners(),
              (this.removeEndListeners = Yt(this.node.current, "keyup", o)),
              Nl("down", (a, l) => {
                this.startPress(a, l);
              });
          },
          n = Yt(this.node.current, "keydown", t),
          r = () => {
            this.isPressing && Nl("cancel", (s, o) => this.cancelPress(s, o));
          },
          i = Yt(this.node.current, "blur", r);
        this.removeAccessibleListeners = Fn(n, i);
      });
  }
  startPress(t, n) {
    this.isPressing = !0;
    const { onTapStart: r, whileTap: i } = this.node.getProps();
    i &&
      this.node.animationState &&
      this.node.animationState.setActive("whileTap", !0),
      r && Y.postRender(() => r(t, n));
  }
  checkPressEnd() {
    return (
      this.removeEndListeners(),
      (this.isPressing = !1),
      this.node.getProps().whileTap &&
        this.node.animationState &&
        this.node.animationState.setActive("whileTap", !1),
      !i0()
    );
  }
  cancelPress(t, n) {
    if (!this.checkPressEnd()) return;
    const { onTapCancel: r } = this.node.getProps();
    r && Y.postRender(() => r(t, n));
  }
  mount() {
    const t = this.node.getProps(),
      n = _n(
        t.globalTapTarget ? window : this.node.current,
        "pointerdown",
        this.startPointerPress,
        { passive: !(t.onTapStart || t.onPointerStart) }
      ),
      r = Yt(this.node.current, "focus", this.startAccessiblePress);
    this.removeStartListeners = Fn(n, r);
  }
  unmount() {
    this.removeStartListeners(),
      this.removeEndListeners(),
      this.removeAccessibleListeners();
  }
}
const Qu = new WeakMap(),
  bl = new WeakMap(),
  Zk = (e) => {
    const t = Qu.get(e.target);
    t && t(e);
  },
  Jk = (e) => {
    e.forEach(Zk);
  };
function eA({ root: e, ...t }) {
  const n = e || document;
  bl.has(n) || bl.set(n, {});
  const r = bl.get(n),
    i = JSON.stringify(t);
  return r[i] || (r[i] = new IntersectionObserver(Jk, { root: e, ...t })), r[i];
}
function tA(e, t, n) {
  const r = eA(t);
  return (
    Qu.set(e, n),
    r.observe(e),
    () => {
      Qu.delete(e), r.unobserve(e);
    }
  );
}
const nA = { some: 0, all: 1 };
class rA extends Kn {
  constructor() {
    super(...arguments), (this.hasEnteredView = !1), (this.isInView = !1);
  }
  startObserver() {
    this.unmount();
    const { viewport: t = {} } = this.node.getProps(),
      { root: n, margin: r, amount: i = "some", once: s } = t,
      o = {
        root: n ? n.current : void 0,
        rootMargin: r,
        threshold: typeof i == "number" ? i : nA[i],
      },
      a = (l) => {
        const { isIntersecting: u } = l;
        if (
          this.isInView === u ||
          ((this.isInView = u), s && !u && this.hasEnteredView)
        )
          return;
        u && (this.hasEnteredView = !0),
          this.node.animationState &&
            this.node.animationState.setActive("whileInView", u);
        const { onViewportEnter: c, onViewportLeave: d } = this.node.getProps(),
          f = u ? c : d;
        f && f(l);
      };
    return tA(this.node.current, o, a);
  }
  mount() {
    this.startObserver();
  }
  update() {
    if (typeof IntersectionObserver > "u") return;
    const { props: t, prevProps: n } = this.node;
    ["amount", "margin", "root"].some(iA(t, n)) && this.startObserver();
  }
  unmount() {}
}
function iA({ viewport: e = {} }, { viewport: t = {} } = {}) {
  return (n) => e[n] !== t[n];
}
const sA = {
    inView: { Feature: rA },
    tap: { Feature: Yk },
    focus: { Feature: Xk },
    hover: { Feature: qk },
  },
  oA = { layout: { ProjectionNode: T0, MeasureLayout: y0 } },
  A0 = w.createContext({
    transformPagePoint: (e) => e,
    isStatic: !1,
    reducedMotion: "never",
  }),
  ba = w.createContext({}),
  Td = typeof window < "u",
  aA = Td ? w.useLayoutEffect : w.useEffect,
  R0 = w.createContext({ strict: !1 });
function lA(e, t, n, r, i) {
  var s, o;
  const { visualElement: a } = w.useContext(ba),
    l = w.useContext(R0),
    u = w.useContext(Cd),
    c = w.useContext(A0).reducedMotion,
    d = w.useRef();
  (r = r || l.renderer),
    !d.current &&
      r &&
      (d.current = r(e, {
        visualState: t,
        parent: a,
        props: n,
        presenceContext: u,
        blockInitialAnimation: u ? u.initial === !1 : !1,
        reducedMotionConfig: c,
      }));
  const f = d.current,
    v = w.useContext(g0);
  f &&
    !f.projection &&
    i &&
    (f.type === "html" || f.type === "svg") &&
    uA(d.current, n, i, v);
  const y = w.useRef(!1);
  w.useInsertionEffect(() => {
    f && y.current && f.update(n, u);
  });
  const m = n[e0],
    x = w.useRef(
      !!m &&
        !(
          !((s = window.MotionHandoffIsComplete) === null || s === void 0) &&
          s.call(window, m)
        ) &&
        ((o = window.MotionHasOptimisedAnimation) === null || o === void 0
          ? void 0
          : o.call(window, m))
    );
  return (
    aA(() => {
      f &&
        ((y.current = !0),
        (window.MotionIsMounted = !0),
        f.updateFeatures(),
        Ed.render(f.render),
        x.current && f.animationState && f.animationState.animateChanges());
    }),
    w.useEffect(() => {
      f &&
        (!x.current && f.animationState && f.animationState.animateChanges(),
        x.current &&
          (queueMicrotask(() => {
            var h;
            (h = window.MotionHandoffMarkAsComplete) === null ||
              h === void 0 ||
              h.call(window, m);
          }),
          (x.current = !1)));
    }),
    f
  );
}
function uA(e, t, n, r) {
  const {
    layoutId: i,
    layout: s,
    drag: o,
    dragConstraints: a,
    layoutScroll: l,
    layoutRoot: u,
  } = t;
  (e.projection = new n(
    e.latestValues,
    t["data-framer-portal-id"] ? void 0 : M0(e.parent)
  )),
    e.projection.setOptions({
      layoutId: i,
      layout: s,
      alwaysMeasureLayout: !!o || (a && jr(a)),
      visualElement: e,
      animationType: typeof s == "string" ? s : "both",
      initialPromotionConfig: r,
      layoutScroll: l,
      layoutRoot: u,
    });
}
function M0(e) {
  if (e) return e.options.allowProjection !== !1 ? e.projection : M0(e.parent);
}
function cA(e, t, n) {
  return w.useCallback(
    (r) => {
      r && e.mount && e.mount(r),
        t && (r ? t.mount(r) : t.unmount()),
        n && (typeof n == "function" ? n(r) : jr(n) && (n.current = r));
    },
    [t]
  );
}
function La(e) {
  return Ma(e.animate) || rd.some((t) => gs(e[t]));
}
function D0(e) {
  return !!(La(e) || e.variants);
}
function dA(e, t) {
  if (La(e)) {
    const { initial: n, animate: r } = e;
    return {
      initial: n === !1 || gs(n) ? n : void 0,
      animate: gs(r) ? r : void 0,
    };
  }
  return e.inherit !== !1 ? t : {};
}
function fA(e) {
  const { initial: t, animate: n } = dA(e, w.useContext(ba));
  return w.useMemo(() => ({ initial: t, animate: n }), [Dp(t), Dp(n)]);
}
function Dp(e) {
  return Array.isArray(e) ? e.join(" ") : e;
}
const Np = {
    animation: [
      "animate",
      "variants",
      "whileHover",
      "whileTap",
      "exit",
      "whileInView",
      "whileFocus",
      "whileDrag",
    ],
    exit: ["exit"],
    drag: ["drag", "dragControls"],
    focus: ["whileFocus"],
    hover: ["whileHover", "onHoverStart", "onHoverEnd"],
    tap: ["whileTap", "onTap", "onTapStart", "onTapCancel"],
    pan: ["onPan", "onPanStart", "onPanSessionStart", "onPanEnd"],
    inView: ["whileInView", "onViewportEnter", "onViewportLeave"],
    layout: ["layout", "layoutId"],
  },
  di = {};
for (const e in Np) di[e] = { isEnabled: (t) => Np[e].some((n) => !!t[n]) };
function hA(e) {
  for (const t in e) di[t] = { ...di[t], ...e[t] };
}
const pA = Symbol.for("motionComponentSymbol");
function mA({
  preloadedFeatures: e,
  createVisualElement: t,
  useRender: n,
  useVisualState: r,
  Component: i,
}) {
  e && hA(e);
  function s(a, l) {
    let u;
    const c = { ...w.useContext(A0), ...a, layoutId: gA(a) },
      { isStatic: d } = c,
      f = fA(a),
      v = r(a, d);
    if (!d && Td) {
      yA();
      const y = vA(c);
      (u = y.MeasureLayout),
        (f.visualElement = lA(i, v, c, t, y.ProjectionNode));
    }
    return P.jsxs(ba.Provider, {
      value: f,
      children: [
        u && f.visualElement
          ? P.jsx(u, { visualElement: f.visualElement, ...c })
          : null,
        n(i, a, cA(v, f.visualElement, l), v, d, f.visualElement),
      ],
    });
  }
  const o = w.forwardRef(s);
  return (o[pA] = i), o;
}
function gA({ layoutId: e }) {
  const t = w.useContext(m0).id;
  return t && e !== void 0 ? t + "-" + e : e;
}
function yA(e, t) {
  w.useContext(R0).strict;
}
function vA(e) {
  const { drag: t, layout: n } = di;
  if (!t && !n) return {};
  const r = { ...t, ...n };
  return {
    MeasureLayout:
      (t != null && t.isEnabled(e)) || (n != null && n.isEnabled(e))
        ? r.MeasureLayout
        : void 0,
    ProjectionNode: r.ProjectionNode,
  };
}
const xA = [
  "animate",
  "circle",
  "defs",
  "desc",
  "ellipse",
  "g",
  "image",
  "line",
  "filter",
  "marker",
  "mask",
  "metadata",
  "path",
  "pattern",
  "polygon",
  "polyline",
  "rect",
  "stop",
  "switch",
  "symbol",
  "svg",
  "text",
  "tspan",
  "use",
  "view",
];
function kd(e) {
  return typeof e != "string" || e.includes("-")
    ? !1
    : !!(xA.indexOf(e) > -1 || /[A-Z]/u.test(e));
}
function N0(e, { style: t, vars: n }, r, i) {
  Object.assign(e.style, t, i && i.getProjectionStyles(r));
  for (const s in n) e.style.setProperty(s, n[s]);
}
const b0 = new Set([
  "baseFrequency",
  "diffuseConstant",
  "kernelMatrix",
  "kernelUnitLength",
  "keySplines",
  "keyTimes",
  "limitingConeAngle",
  "markerHeight",
  "markerWidth",
  "numOctaves",
  "targetX",
  "targetY",
  "surfaceScale",
  "specularConstant",
  "specularExponent",
  "stdDeviation",
  "tableValues",
  "viewBox",
  "gradientTransform",
  "pathLength",
  "startOffset",
  "textLength",
  "lengthAdjust",
]);
function L0(e, t, n, r) {
  N0(e, t, void 0, r);
  for (const i in t.attrs) e.setAttribute(b0.has(i) ? i : Pd(i), t.attrs[i]);
}
function O0(e, { layout: t, layoutId: n }) {
  return (
    wr.has(e) ||
    e.startsWith("origin") ||
    ((t || n !== void 0) && (!!ta[e] || e === "opacity"))
  );
}
function Ad(e, t, n) {
  var r;
  const { style: i } = e,
    s = {};
  for (const o in i)
    (je(i[o]) ||
      (t.style && je(t.style[o])) ||
      O0(o, e) ||
      ((r = n == null ? void 0 : n.getValue(o)) === null || r === void 0
        ? void 0
        : r.liveStyle) !== void 0) &&
      (s[o] = i[o]);
  return s;
}
function j0(e, t, n) {
  const r = Ad(e, t, n);
  for (const i in e)
    if (je(e[i]) || je(t[i])) {
      const s =
        Ds.indexOf(i) !== -1
          ? "attr" + i.charAt(0).toUpperCase() + i.substring(1)
          : i;
      r[s] = e[i];
    }
  return r;
}
function wA(e) {
  const t = w.useRef(null);
  return t.current === null && (t.current = e()), t.current;
}
function SA(
  { scrapeMotionValuesFromProps: e, createRenderState: t, onMount: n },
  r,
  i,
  s
) {
  const o = { latestValues: PA(r, i, s, e), renderState: t() };
  return n && (o.mount = (a) => n(r, a, o)), o;
}
const I0 = (e) => (t, n) => {
  const r = w.useContext(ba),
    i = w.useContext(Cd),
    s = () => SA(e, t, r, i);
  return n ? s() : wA(s);
};
function PA(e, t, n, r) {
  const i = {},
    s = r(e, {});
  for (const f in s) i[f] = Co(s[f]);
  let { initial: o, animate: a } = e;
  const l = La(e),
    u = D0(e);
  t &&
    u &&
    !l &&
    e.inherit !== !1 &&
    (o === void 0 && (o = t.initial), a === void 0 && (a = t.animate));
  let c = n ? n.initial === !1 : !1;
  c = c || o === !1;
  const d = c ? a : o;
  if (d && typeof d != "boolean" && !Ma(d)) {
    const f = Array.isArray(d) ? d : [d];
    for (let v = 0; v < f.length; v++) {
      const y = td(e, f[v]);
      if (y) {
        const { transitionEnd: m, transition: x, ...h } = y;
        for (const p in h) {
          let g = h[p];
          if (Array.isArray(g)) {
            const S = c ? g.length - 1 : 0;
            g = g[S];
          }
          g !== null && (i[p] = g);
        }
        for (const p in m) i[p] = m[p];
      }
    }
  }
  return i;
}
const Rd = () => ({ style: {}, transform: {}, transformOrigin: {}, vars: {} }),
  F0 = () => ({ ...Rd(), attrs: {} }),
  _0 = (e, t) => (t && typeof e == "number" ? t.transform(e) : e),
  CA = {
    x: "translateX",
    y: "translateY",
    z: "translateZ",
    transformPerspective: "perspective",
  },
  EA = Ds.length;
function TA(e, t, n) {
  let r = "",
    i = !0;
  for (let s = 0; s < EA; s++) {
    const o = Ds[s],
      a = e[o];
    if (a === void 0) continue;
    let l = !0;
    if (
      (typeof a == "number"
        ? (l = a === (o.startsWith("scale") ? 1 : 0))
        : (l = parseFloat(a) === 0),
      !l || n)
    ) {
      const u = _0(a, dd[o]);
      if (!l) {
        i = !1;
        const c = CA[o] || o;
        r += `${c}(${u}) `;
      }
      n && (t[o] = u);
    }
  }
  return (r = r.trim()), n ? (r = n(t, i ? "" : r)) : i && (r = "none"), r;
}
function Md(e, t, n) {
  const { style: r, vars: i, transformOrigin: s } = e;
  let o = !1,
    a = !1;
  for (const l in t) {
    const u = t[l];
    if (wr.has(l)) {
      o = !0;
      continue;
    } else if (Mv(l)) {
      i[l] = u;
      continue;
    } else {
      const c = _0(u, dd[l]);
      l.startsWith("origin") ? ((a = !0), (s[l] = c)) : (r[l] = c);
    }
  }
  if (
    (t.transform ||
      (o || n
        ? (r.transform = TA(t, e.transform, n))
        : r.transform && (r.transform = "none")),
    a)
  ) {
    const { originX: l = "50%", originY: u = "50%", originZ: c = 0 } = s;
    r.transformOrigin = `${l} ${u} ${c}`;
  }
}
function bp(e, t, n) {
  return typeof e == "string" ? e : V.transform(t + n * e);
}
function kA(e, t, n) {
  const r = bp(t, e.x, e.width),
    i = bp(n, e.y, e.height);
  return `${r} ${i}`;
}
const AA = { offset: "stroke-dashoffset", array: "stroke-dasharray" },
  RA = { offset: "strokeDashoffset", array: "strokeDasharray" };
function MA(e, t, n = 1, r = 0, i = !0) {
  e.pathLength = 1;
  const s = i ? AA : RA;
  e[s.offset] = V.transform(-r);
  const o = V.transform(t),
    a = V.transform(n);
  e[s.array] = `${o} ${a}`;
}
function Dd(
  e,
  {
    attrX: t,
    attrY: n,
    attrScale: r,
    originX: i,
    originY: s,
    pathLength: o,
    pathSpacing: a = 1,
    pathOffset: l = 0,
    ...u
  },
  c,
  d
) {
  if ((Md(e, u, d), c)) {
    e.style.viewBox && (e.attrs.viewBox = e.style.viewBox);
    return;
  }
  (e.attrs = e.style), (e.style = {});
  const { attrs: f, style: v, dimensions: y } = e;
  f.transform && (y && (v.transform = f.transform), delete f.transform),
    y &&
      (i !== void 0 || s !== void 0 || v.transform) &&
      (v.transformOrigin = kA(
        y,
        i !== void 0 ? i : 0.5,
        s !== void 0 ? s : 0.5
      )),
    t !== void 0 && (f.x = t),
    n !== void 0 && (f.y = n),
    r !== void 0 && (f.scale = r),
    o !== void 0 && MA(f, o, a, l, !1);
}
const Nd = (e) => typeof e == "string" && e.toLowerCase() === "svg",
  DA = {
    useVisualState: I0({
      scrapeMotionValuesFromProps: j0,
      createRenderState: F0,
      onMount: (e, t, { renderState: n, latestValues: r }) => {
        Y.read(() => {
          try {
            n.dimensions =
              typeof t.getBBox == "function"
                ? t.getBBox()
                : t.getBoundingClientRect();
          } catch {
            n.dimensions = { x: 0, y: 0, width: 0, height: 0 };
          }
        }),
          Y.render(() => {
            Dd(n, r, Nd(t.tagName), e.transformTemplate), L0(t, n);
          });
      },
    }),
  },
  NA = {
    useVisualState: I0({
      scrapeMotionValuesFromProps: Ad,
      createRenderState: Rd,
    }),
  };
function V0(e, t, n) {
  for (const r in t) !je(t[r]) && !O0(r, n) && (e[r] = t[r]);
}
function bA({ transformTemplate: e }, t) {
  return w.useMemo(() => {
    const n = Rd();
    return Md(n, t, e), Object.assign({}, n.vars, n.style);
  }, [t]);
}
function LA(e, t) {
  const n = e.style || {},
    r = {};
  return V0(r, n, e), Object.assign(r, bA(e, t)), r;
}
function OA(e, t) {
  const n = {},
    r = LA(e, t);
  return (
    e.drag &&
      e.dragListener !== !1 &&
      ((n.draggable = !1),
      (r.userSelect = r.WebkitUserSelect = r.WebkitTouchCallout = "none"),
      (r.touchAction =
        e.drag === !0 ? "none" : `pan-${e.drag === "x" ? "y" : "x"}`)),
    e.tabIndex === void 0 &&
      (e.onTap || e.onTapStart || e.whileTap) &&
      (n.tabIndex = 0),
    (n.style = r),
    n
  );
}
const jA = new Set([
  "animate",
  "exit",
  "variants",
  "initial",
  "style",
  "values",
  "variants",
  "transition",
  "transformTemplate",
  "custom",
  "inherit",
  "onBeforeLayoutMeasure",
  "onAnimationStart",
  "onAnimationComplete",
  "onUpdate",
  "onDragStart",
  "onDrag",
  "onDragEnd",
  "onMeasureDragConstraints",
  "onDirectionLock",
  "onDragTransitionEnd",
  "_dragX",
  "_dragY",
  "onHoverStart",
  "onHoverEnd",
  "onViewportEnter",
  "onViewportLeave",
  "globalTapTarget",
  "ignoreStrict",
  "viewport",
]);
function na(e) {
  return (
    e.startsWith("while") ||
    (e.startsWith("drag") && e !== "draggable") ||
    e.startsWith("layout") ||
    e.startsWith("onTap") ||
    e.startsWith("onPan") ||
    e.startsWith("onLayout") ||
    jA.has(e)
  );
}
let z0 = (e) => !na(e);
function IA(e) {
  e && (z0 = (t) => (t.startsWith("on") ? !na(t) : e(t)));
}
try {
  IA(require("@emotion/is-prop-valid").default);
} catch {}
function FA(e, t, n) {
  const r = {};
  for (const i in e)
    (i === "values" && typeof e.values == "object") ||
      ((z0(i) ||
        (n === !0 && na(i)) ||
        (!t && !na(i)) ||
        (e.draggable && i.startsWith("onDrag"))) &&
        (r[i] = e[i]));
  return r;
}
function _A(e, t, n, r) {
  const i = w.useMemo(() => {
    const s = F0();
    return (
      Dd(s, t, Nd(r), e.transformTemplate),
      { ...s.attrs, style: { ...s.style } }
    );
  }, [t]);
  if (e.style) {
    const s = {};
    V0(s, e.style, e), (i.style = { ...s, ...i.style });
  }
  return i;
}
function VA(e = !1) {
  return (n, r, i, { latestValues: s }, o) => {
    const l = (kd(n) ? _A : OA)(r, s, o, n),
      u = FA(r, typeof n == "string", e),
      c = n !== w.Fragment ? { ...u, ...l, ref: i } : {},
      { children: d } = r,
      f = w.useMemo(() => (je(d) ? d.get() : d), [d]);
    return w.createElement(n, { ...c, children: f });
  };
}
function zA(e, t) {
  return function (r, { forwardMotionProps: i } = { forwardMotionProps: !1 }) {
    const o = {
      ...(kd(r) ? DA : NA),
      preloadedFeatures: e,
      useRender: VA(i),
      createVisualElement: t,
      Component: r,
    };
    return mA(o);
  };
}
const Gu = { current: null },
  B0 = { current: !1 };
function BA() {
  if (((B0.current = !0), !!Td))
    if (window.matchMedia) {
      const e = window.matchMedia("(prefers-reduced-motion)"),
        t = () => (Gu.current = e.matches);
      e.addListener(t), t();
    } else Gu.current = !1;
}
function UA(e, t, n) {
  for (const r in t) {
    const i = t[r],
      s = n[r];
    if (je(i)) e.addValue(r, i);
    else if (je(s)) e.addValue(r, xs(i, { owner: e }));
    else if (s !== i)
      if (e.hasValue(r)) {
        const o = e.getValue(r);
        o.liveStyle === !0 ? o.jump(i) : o.hasAnimated || o.set(i);
      } else {
        const o = e.getStaticValue(r);
        e.addValue(r, xs(o !== void 0 ? o : i, { owner: e }));
      }
  }
  for (const r in n) t[r] === void 0 && e.removeValue(r);
  return t;
}
const Lp = new WeakMap(),
  $A = [...bv, Le, Un],
  WA = (e) => $A.find(Nv(e)),
  Op = [
    "AnimationStart",
    "AnimationComplete",
    "Update",
    "BeforeLayoutMeasure",
    "LayoutMeasure",
    "LayoutAnimationStart",
    "LayoutAnimationComplete",
  ];
class HA {
  scrapeMotionValuesFromProps(t, n, r) {
    return {};
  }
  constructor(
    {
      parent: t,
      props: n,
      presenceContext: r,
      reducedMotionConfig: i,
      blockInitialAnimation: s,
      visualState: o,
    },
    a = {}
  ) {
    (this.current = null),
      (this.children = new Set()),
      (this.isVariantNode = !1),
      (this.isControllingVariants = !1),
      (this.shouldReduceMotion = null),
      (this.values = new Map()),
      (this.KeyframeResolver = ld),
      (this.features = {}),
      (this.valueSubscriptions = new Map()),
      (this.prevMotionValues = {}),
      (this.events = {}),
      (this.propEventSubscriptions = {}),
      (this.notifyUpdate = () => this.notify("Update", this.latestValues)),
      (this.render = () => {
        this.current &&
          (this.triggerBuild(),
          this.renderInstance(
            this.current,
            this.renderState,
            this.props.style,
            this.projection
          ));
      }),
      (this.renderScheduledAt = 0),
      (this.scheduleRender = () => {
        const f = zt.now();
        this.renderScheduledAt < f &&
          ((this.renderScheduledAt = f), Y.render(this.render, !1, !0));
      });
    const { latestValues: l, renderState: u } = o;
    (this.latestValues = l),
      (this.baseTarget = { ...l }),
      (this.initialValues = n.initial ? { ...l } : {}),
      (this.renderState = u),
      (this.parent = t),
      (this.props = n),
      (this.presenceContext = r),
      (this.depth = t ? t.depth + 1 : 0),
      (this.reducedMotionConfig = i),
      (this.options = a),
      (this.blockInitialAnimation = !!s),
      (this.isControllingVariants = La(n)),
      (this.isVariantNode = D0(n)),
      this.isVariantNode && (this.variantChildren = new Set()),
      (this.manuallyAnimateOnMount = !!(t && t.current));
    const { willChange: c, ...d } = this.scrapeMotionValuesFromProps(
      n,
      {},
      this
    );
    for (const f in d) {
      const v = d[f];
      l[f] !== void 0 && je(v) && v.set(l[f], !1);
    }
  }
  mount(t) {
    (this.current = t),
      Lp.set(t, this),
      this.projection && !this.projection.instance && this.projection.mount(t),
      this.parent &&
        this.isVariantNode &&
        !this.isControllingVariants &&
        (this.removeFromVariantTree = this.parent.addVariantChild(this)),
      this.values.forEach((n, r) => this.bindToMotionValue(r, n)),
      B0.current || BA(),
      (this.shouldReduceMotion =
        this.reducedMotionConfig === "never"
          ? !1
          : this.reducedMotionConfig === "always"
          ? !0
          : Gu.current),
      this.parent && this.parent.children.add(this),
      this.update(this.props, this.presenceContext);
  }
  unmount() {
    Lp.delete(this.current),
      this.projection && this.projection.unmount(),
      Bn(this.notifyUpdate),
      Bn(this.render),
      this.valueSubscriptions.forEach((t) => t()),
      this.valueSubscriptions.clear(),
      this.removeFromVariantTree && this.removeFromVariantTree(),
      this.parent && this.parent.children.delete(this);
    for (const t in this.events) this.events[t].clear();
    for (const t in this.features) {
      const n = this.features[t];
      n && (n.unmount(), (n.isMounted = !1));
    }
    this.current = null;
  }
  bindToMotionValue(t, n) {
    this.valueSubscriptions.has(t) && this.valueSubscriptions.get(t)();
    const r = wr.has(t),
      i = n.on("change", (a) => {
        (this.latestValues[t] = a),
          this.props.onUpdate && Y.preRender(this.notifyUpdate),
          r && this.projection && (this.projection.isTransformDirty = !0);
      }),
      s = n.on("renderRequest", this.scheduleRender);
    let o;
    window.MotionCheckAppearSync &&
      (o = window.MotionCheckAppearSync(this, t, n)),
      this.valueSubscriptions.set(t, () => {
        i(), s(), o && o(), n.owner && n.stop();
      });
  }
  sortNodePosition(t) {
    return !this.current ||
      !this.sortInstanceNodePosition ||
      this.type !== t.type
      ? 0
      : this.sortInstanceNodePosition(this.current, t.current);
  }
  updateFeatures() {
    let t = "animation";
    for (t in di) {
      const n = di[t];
      if (!n) continue;
      const { isEnabled: r, Feature: i } = n;
      if (
        (!this.features[t] &&
          i &&
          r(this.props) &&
          (this.features[t] = new i(this)),
        this.features[t])
      ) {
        const s = this.features[t];
        s.isMounted ? s.update() : (s.mount(), (s.isMounted = !0));
      }
    }
  }
  triggerBuild() {
    this.build(this.renderState, this.latestValues, this.props);
  }
  measureViewportBox() {
    return this.current
      ? this.measureInstanceViewportBox(this.current, this.props)
      : pe();
  }
  getStaticValue(t) {
    return this.latestValues[t];
  }
  setStaticValue(t, n) {
    this.latestValues[t] = n;
  }
  update(t, n) {
    (t.transformTemplate || this.props.transformTemplate) &&
      this.scheduleRender(),
      (this.prevProps = this.props),
      (this.props = t),
      (this.prevPresenceContext = this.presenceContext),
      (this.presenceContext = n);
    for (let r = 0; r < Op.length; r++) {
      const i = Op[r];
      this.propEventSubscriptions[i] &&
        (this.propEventSubscriptions[i](),
        delete this.propEventSubscriptions[i]);
      const s = "on" + i,
        o = t[s];
      o && (this.propEventSubscriptions[i] = this.on(i, o));
    }
    (this.prevMotionValues = UA(
      this,
      this.scrapeMotionValuesFromProps(t, this.prevProps, this),
      this.prevMotionValues
    )),
      this.handleChildMotionValue && this.handleChildMotionValue();
  }
  getProps() {
    return this.props;
  }
  getVariant(t) {
    return this.props.variants ? this.props.variants[t] : void 0;
  }
  getDefaultTransition() {
    return this.props.transition;
  }
  getTransformPagePoint() {
    return this.props.transformPagePoint;
  }
  getClosestVariantNode() {
    return this.isVariantNode
      ? this
      : this.parent
      ? this.parent.getClosestVariantNode()
      : void 0;
  }
  addVariantChild(t) {
    const n = this.getClosestVariantNode();
    if (n)
      return (
        n.variantChildren && n.variantChildren.add(t),
        () => n.variantChildren.delete(t)
      );
  }
  addValue(t, n) {
    const r = this.values.get(t);
    n !== r &&
      (r && this.removeValue(t),
      this.bindToMotionValue(t, n),
      this.values.set(t, n),
      (this.latestValues[t] = n.get()));
  }
  removeValue(t) {
    this.values.delete(t);
    const n = this.valueSubscriptions.get(t);
    n && (n(), this.valueSubscriptions.delete(t)),
      delete this.latestValues[t],
      this.removeValueFromRenderState(t, this.renderState);
  }
  hasValue(t) {
    return this.values.has(t);
  }
  getValue(t, n) {
    if (this.props.values && this.props.values[t]) return this.props.values[t];
    let r = this.values.get(t);
    return (
      r === void 0 &&
        n !== void 0 &&
        ((r = xs(n === null ? void 0 : n, { owner: this })),
        this.addValue(t, r)),
      r
    );
  }
  readValue(t, n) {
    var r;
    let i =
      this.latestValues[t] !== void 0 || !this.current
        ? this.latestValues[t]
        : (r = this.getBaseTargetFromProps(this.props, t)) !== null &&
          r !== void 0
        ? r
        : this.readValueFromInstance(this.current, t, this.options);
    return (
      i != null &&
        (typeof i == "string" && (Av(i) || kv(i))
          ? (i = parseFloat(i))
          : !WA(i) && Un.test(n) && (i = zv(t, n)),
        this.setBaseTarget(t, je(i) ? i.get() : i)),
      je(i) ? i.get() : i
    );
  }
  setBaseTarget(t, n) {
    this.baseTarget[t] = n;
  }
  getBaseTarget(t) {
    var n;
    const { initial: r } = this.props;
    let i;
    if (typeof r == "string" || typeof r == "object") {
      const o = td(
        this.props,
        r,
        (n = this.presenceContext) === null || n === void 0 ? void 0 : n.custom
      );
      o && (i = o[t]);
    }
    if (r && i !== void 0) return i;
    const s = this.getBaseTargetFromProps(this.props, t);
    return s !== void 0 && !je(s)
      ? s
      : this.initialValues[t] !== void 0 && i === void 0
      ? void 0
      : this.baseTarget[t];
  }
  on(t, n) {
    return this.events[t] || (this.events[t] = new Sd()), this.events[t].add(n);
  }
  notify(t, ...n) {
    this.events[t] && this.events[t].notify(...n);
  }
}
class U0 extends HA {
  constructor() {
    super(...arguments), (this.KeyframeResolver = Bv);
  }
  sortInstanceNodePosition(t, n) {
    return t.compareDocumentPosition(n) & 2 ? 1 : -1;
  }
  getBaseTargetFromProps(t, n) {
    return t.style ? t.style[n] : void 0;
  }
  removeValueFromRenderState(t, { vars: n, style: r }) {
    delete n[t], delete r[t];
  }
  handleChildMotionValue() {
    this.childSubscription &&
      (this.childSubscription(), delete this.childSubscription);
    const { children: t } = this.props;
    je(t) &&
      (this.childSubscription = t.on("change", (n) => {
        this.current && (this.current.textContent = `${n}`);
      }));
  }
}
function KA(e) {
  return window.getComputedStyle(e);
}
class QA extends U0 {
  constructor() {
    super(...arguments), (this.type = "html"), (this.renderInstance = N0);
  }
  readValueFromInstance(t, n) {
    if (wr.has(n)) {
      const r = fd(n);
      return (r && r.default) || 0;
    } else {
      const r = KA(t),
        i = (Mv(n) ? r.getPropertyValue(n) : r[n]) || 0;
      return typeof i == "string" ? i.trim() : i;
    }
  }
  measureInstanceViewportBox(t, { transformPagePoint: n }) {
    return h0(t, n);
  }
  build(t, n, r) {
    Md(t, n, r.transformTemplate);
  }
  scrapeMotionValuesFromProps(t, n, r) {
    return Ad(t, n, r);
  }
}
class GA extends U0 {
  constructor() {
    super(...arguments),
      (this.type = "svg"),
      (this.isSVGTag = !1),
      (this.measureInstanceViewportBox = pe);
  }
  getBaseTargetFromProps(t, n) {
    return t[n];
  }
  readValueFromInstance(t, n) {
    if (wr.has(n)) {
      const r = fd(n);
      return (r && r.default) || 0;
    }
    return (n = b0.has(n) ? n : Pd(n)), t.getAttribute(n);
  }
  scrapeMotionValuesFromProps(t, n, r) {
    return j0(t, n, r);
  }
  build(t, n, r) {
    Dd(t, n, this.isSVGTag, r.transformTemplate);
  }
  renderInstance(t, n, r, i) {
    L0(t, n, r, i);
  }
  mount(t) {
    (this.isSVGTag = Nd(t.tagName)), super.mount(t);
  }
}
const qA = (e, t) =>
    kd(e) ? new GA(t) : new QA(t, { allowProjection: e !== w.Fragment }),
  XA = zA({ ...OT, ...sA, ...Gk, ...oA }, qA),
  ra = bC(XA);
function YA(e) {
  return Object.prototype.toString.call(e) === "[object Object]";
}
function jp(e) {
  return YA(e) || Array.isArray(e);
}
function ZA() {
  return !!(
    typeof window < "u" &&
    window.document &&
    window.document.createElement
  );
}
function bd(e, t) {
  const n = Object.keys(e),
    r = Object.keys(t);
  if (n.length !== r.length) return !1;
  const i = JSON.stringify(Object.keys(e.breakpoints || {})),
    s = JSON.stringify(Object.keys(t.breakpoints || {}));
  return i !== s
    ? !1
    : n.every((o) => {
        const a = e[o],
          l = t[o];
        return typeof a == "function"
          ? `${a}` == `${l}`
          : !jp(a) || !jp(l)
          ? a === l
          : bd(a, l);
      });
}
function Ip(e) {
  return e
    .concat()
    .sort((t, n) => (t.name > n.name ? 1 : -1))
    .map((t) => t.options);
}
function JA(e, t) {
  if (e.length !== t.length) return !1;
  const n = Ip(e),
    r = Ip(t);
  return n.every((i, s) => {
    const o = r[s];
    return bd(i, o);
  });
}
function Ld(e) {
  return typeof e == "number";
}
function qu(e) {
  return typeof e == "string";
}
function Oa(e) {
  return typeof e == "boolean";
}
function Fp(e) {
  return Object.prototype.toString.call(e) === "[object Object]";
}
function le(e) {
  return Math.abs(e);
}
function Od(e) {
  return Math.sign(e);
}
function qi(e, t) {
  return le(e - t);
}
function eR(e, t) {
  if (e === 0 || t === 0 || le(e) <= le(t)) return 0;
  const n = qi(le(e), le(t));
  return le(n / e);
}
function ws(e) {
  return Ss(e).map(Number);
}
function Rt(e) {
  return e[Os(e)];
}
function Os(e) {
  return Math.max(0, e.length - 1);
}
function jd(e, t) {
  return t === Os(e);
}
function _p(e, t = 0) {
  return Array.from(Array(e), (n, r) => t + r);
}
function Ss(e) {
  return Object.keys(e);
}
function $0(e, t) {
  return [e, t].reduce(
    (n, r) => (
      Ss(r).forEach((i) => {
        const s = n[i],
          o = r[i],
          a = Fp(s) && Fp(o);
        n[i] = a ? $0(s, o) : o;
      }),
      n
    ),
    {}
  );
}
function Xu(e, t) {
  return typeof t.MouseEvent < "u" && e instanceof t.MouseEvent;
}
function tR(e, t) {
  const n = { start: r, center: i, end: s };
  function r() {
    return 0;
  }
  function i(l) {
    return s(l) / 2;
  }
  function s(l) {
    return t - l;
  }
  function o(l, u) {
    return qu(e) ? n[e](l) : e(t, l, u);
  }
  return { measure: o };
}
function Ps() {
  let e = [];
  function t(i, s, o, a = { passive: !0 }) {
    let l;
    if ("addEventListener" in i)
      i.addEventListener(s, o, a), (l = () => i.removeEventListener(s, o, a));
    else {
      const u = i;
      u.addListener(o), (l = () => u.removeListener(o));
    }
    return e.push(l), r;
  }
  function n() {
    e = e.filter((i) => i());
  }
  const r = { add: t, clear: n };
  return r;
}
function nR(e, t, n, r) {
  const i = Ps(),
    s = 1e3 / 60;
  let o = null,
    a = 0,
    l = 0;
  function u() {
    i.add(e, "visibilitychange", () => {
      e.hidden && y();
    });
  }
  function c() {
    v(), i.clear();
  }
  function d(x) {
    if (!l) return;
    o || (o = x);
    const h = x - o;
    for (o = x, a += h; a >= s; ) n(s), (a -= s);
    const p = a / s;
    r(p), l && t.requestAnimationFrame(d);
  }
  function f() {
    l || (l = t.requestAnimationFrame(d));
  }
  function v() {
    t.cancelAnimationFrame(l), (o = null), (a = 0), (l = 0);
  }
  function y() {
    (o = null), (a = 0);
  }
  return {
    init: u,
    destroy: c,
    start: f,
    stop: v,
    update: () => n(s),
    render: r,
  };
}
function rR(e, t) {
  const n = t === "rtl",
    r = e === "y",
    i = r ? "y" : "x",
    s = r ? "x" : "y",
    o = !r && n ? -1 : 1,
    a = c(),
    l = d();
  function u(y) {
    const { height: m, width: x } = y;
    return r ? m : x;
  }
  function c() {
    return r ? "top" : n ? "right" : "left";
  }
  function d() {
    return r ? "bottom" : n ? "left" : "right";
  }
  function f(y) {
    return y * o;
  }
  return {
    scroll: i,
    cross: s,
    startEdge: a,
    endEdge: l,
    measureSize: u,
    direction: f,
  };
}
function yr(e = 0, t = 0) {
  const n = le(e - t);
  function r(u) {
    return u < e;
  }
  function i(u) {
    return u > t;
  }
  function s(u) {
    return r(u) || i(u);
  }
  function o(u) {
    return s(u) ? (r(u) ? e : t) : u;
  }
  function a(u) {
    return n ? u - n * Math.ceil((u - t) / n) : u;
  }
  return {
    length: n,
    max: t,
    min: e,
    constrain: o,
    reachedAny: s,
    reachedMax: i,
    reachedMin: r,
    removeOffset: a,
  };
}
function W0(e, t, n) {
  const { constrain: r } = yr(0, e),
    i = e + 1;
  let s = o(t);
  function o(f) {
    return n ? le((i + f) % i) : r(f);
  }
  function a() {
    return s;
  }
  function l(f) {
    return (s = o(f)), d;
  }
  function u(f) {
    return c().set(a() + f);
  }
  function c() {
    return W0(e, a(), n);
  }
  const d = { get: a, set: l, add: u, clone: c };
  return d;
}
function iR(e, t, n, r, i, s, o, a, l, u, c, d, f, v, y, m, x, h, p) {
  const { cross: g, direction: S } = e,
    C = ["INPUT", "SELECT", "TEXTAREA"],
    k = { passive: !1 },
    T = Ps(),
    E = Ps(),
    D = yr(50, 225).constrain(v.measure(20)),
    N = { mouse: 300, touch: 400 },
    j = { mouse: 500, touch: 600 },
    I = y ? 43 : 25;
  let Z = !1,
    b = 0,
    H = 0,
    G = !1,
    B = !1,
    R = !1,
    L = !1;
  function F(_) {
    if (!p) return;
    function J(Ve) {
      (Oa(p) || p(_, Ve)) && Ye(Ve);
    }
    const ye = t;
    T.add(ye, "dragstart", (Ve) => Ve.preventDefault(), k)
      .add(ye, "touchmove", () => {}, k)
      .add(ye, "touchend", () => {})
      .add(ye, "touchstart", J)
      .add(ye, "mousedown", J)
      .add(ye, "touchcancel", _e)
      .add(ye, "contextmenu", _e)
      .add(ye, "click", $t, !0);
  }
  function z() {
    T.clear(), E.clear();
  }
  function Q() {
    const _ = L ? n : t;
    E.add(_, "touchmove", Pe, k)
      .add(_, "touchend", _e)
      .add(_, "mousemove", Pe, k)
      .add(_, "mouseup", _e);
  }
  function xe(_) {
    const J = _.nodeName || "";
    return C.includes(J);
  }
  function ge() {
    return (y ? j : N)[L ? "mouse" : "touch"];
  }
  function Ut(_, J) {
    const ye = d.add(Od(_) * -1),
      Ve = c.byDistance(_, !y).distance;
    return y || le(_) < D
      ? Ve
      : x && J
      ? Ve * 0.5
      : c.byIndex(ye.get(), 0).distance;
  }
  function Ye(_) {
    const J = Xu(_, r);
    (L = J),
      (R = y && J && !_.buttons && Z),
      (Z = qi(i.get(), o.get()) >= 2),
      !(J && _.button !== 0) &&
        (xe(_.target) ||
          ((G = !0),
          s.pointerDown(_),
          u.useFriction(0).useDuration(0),
          i.set(o),
          Q(),
          (b = s.readPoint(_)),
          (H = s.readPoint(_, g)),
          f.emit("pointerDown")));
  }
  function Pe(_) {
    if (!Xu(_, r) && _.touches.length >= 2) return _e(_);
    const ye = s.readPoint(_),
      Ve = s.readPoint(_, g),
      Dt = qi(ye, b),
      Wt = qi(Ve, H);
    if (!B && !L && (!_.cancelable || ((B = Dt > Wt), !B))) return _e(_);
    const un = s.pointerMove(_);
    Dt > m && (R = !0),
      u.useFriction(0.3).useDuration(0.75),
      a.start(),
      i.add(S(un)),
      _.preventDefault();
  }
  function _e(_) {
    const ye = c.byDistance(0, !1).index !== d.get(),
      Ve = s.pointerUp(_) * ge(),
      Dt = Ut(S(Ve), ye),
      Wt = eR(Ve, Dt),
      un = I - 10 * Wt,
      cn = h + Wt / 50;
    (B = !1),
      (G = !1),
      E.clear(),
      u.useDuration(un).useFriction(cn),
      l.distance(Dt, !y),
      (L = !1),
      f.emit("pointerUp");
  }
  function $t(_) {
    R && (_.stopPropagation(), _.preventDefault(), (R = !1));
  }
  function lt() {
    return G;
  }
  return { init: F, destroy: z, pointerDown: lt };
}
function sR(e, t) {
  let r, i;
  function s(d) {
    return d.timeStamp;
  }
  function o(d, f) {
    const y = `client${(f || e.scroll) === "x" ? "X" : "Y"}`;
    return (Xu(d, t) ? d : d.touches[0])[y];
  }
  function a(d) {
    return (r = d), (i = d), o(d);
  }
  function l(d) {
    const f = o(d) - o(i),
      v = s(d) - s(r) > 170;
    return (i = d), v && (r = d), f;
  }
  function u(d) {
    if (!r || !i) return 0;
    const f = o(i) - o(r),
      v = s(d) - s(r),
      y = s(d) - s(i) > 170,
      m = f / v;
    return v && !y && le(m) > 0.1 ? m : 0;
  }
  return { pointerDown: a, pointerMove: l, pointerUp: u, readPoint: o };
}
function oR() {
  function e(n) {
    const { offsetTop: r, offsetLeft: i, offsetWidth: s, offsetHeight: o } = n;
    return {
      top: r,
      right: i + s,
      bottom: r + o,
      left: i,
      width: s,
      height: o,
    };
  }
  return { measure: e };
}
function aR(e) {
  function t(r) {
    return e * (r / 100);
  }
  return { measure: t };
}
function lR(e, t, n, r, i, s, o) {
  const a = [e].concat(r);
  let l,
    u,
    c = [],
    d = !1;
  function f(x) {
    return i.measureSize(o.measure(x));
  }
  function v(x) {
    if (!s) return;
    (u = f(e)), (c = r.map(f));
    function h(p) {
      for (const g of p) {
        if (d) return;
        const S = g.target === e,
          C = r.indexOf(g.target),
          k = S ? u : c[C],
          T = f(S ? e : r[C]);
        if (le(T - k) >= 0.5) {
          x.reInit(), t.emit("resize");
          break;
        }
      }
    }
    (l = new ResizeObserver((p) => {
      (Oa(s) || s(x, p)) && h(p);
    })),
      n.requestAnimationFrame(() => {
        a.forEach((p) => l.observe(p));
      });
  }
  function y() {
    (d = !0), l && l.disconnect();
  }
  return { init: v, destroy: y };
}
function uR(e, t, n, r, i, s) {
  let o = 0,
    a = 0,
    l = i,
    u = s,
    c = e.get(),
    d = 0;
  function f(k) {
    const T = k / 1e3,
      E = l * T,
      D = r.get() - e.get(),
      N = !l;
    let j = 0;
    return (
      N
        ? ((o = 0), n.set(r), e.set(r), (j = D))
        : (n.set(e),
          (o += D / E),
          (o *= u),
          (c += o),
          e.add(o * T),
          (j = c - d)),
      (a = Od(j)),
      (d = c),
      C
    );
  }
  function v() {
    const k = r.get() - t.get();
    return le(k) < 0.001;
  }
  function y() {
    return l;
  }
  function m() {
    return a;
  }
  function x() {
    return o;
  }
  function h() {
    return g(i);
  }
  function p() {
    return S(s);
  }
  function g(k) {
    return (l = k), C;
  }
  function S(k) {
    return (u = k), C;
  }
  const C = {
    direction: m,
    duration: y,
    velocity: x,
    seek: f,
    settled: v,
    useBaseFriction: p,
    useBaseDuration: h,
    useFriction: S,
    useDuration: g,
  };
  return C;
}
function cR(e, t, n, r, i) {
  const s = i.measure(10),
    o = i.measure(50),
    a = yr(0.1, 0.99);
  let l = !1;
  function u() {
    return !(l || !e.reachedAny(n.get()) || !e.reachedAny(t.get()));
  }
  function c(v) {
    if (!u()) return;
    const y = e.reachedMin(t.get()) ? "min" : "max",
      m = le(e[y] - t.get()),
      x = n.get() - t.get(),
      h = a.constrain(m / o);
    n.subtract(x * h),
      !v &&
        le(x) < s &&
        (n.set(e.constrain(n.get())), r.useDuration(25).useBaseFriction());
  }
  function d(v) {
    l = !v;
  }
  return { shouldConstrain: u, constrain: c, toggleActive: d };
}
function dR(e, t, n, r, i) {
  const s = yr(-t + e, 0),
    o = d(),
    a = c(),
    l = f();
  function u(y, m) {
    return qi(y, m) < 1;
  }
  function c() {
    const y = o[0],
      m = Rt(o),
      x = o.lastIndexOf(y),
      h = o.indexOf(m) + 1;
    return yr(x, h);
  }
  function d() {
    return n
      .map((y, m) => {
        const { min: x, max: h } = s,
          p = s.constrain(y),
          g = !m,
          S = jd(n, m);
        return g ? h : S || u(x, p) ? x : u(h, p) ? h : p;
      })
      .map((y) => parseFloat(y.toFixed(3)));
  }
  function f() {
    if (t <= e + i) return [s.max];
    if (r === "keepSnaps") return o;
    const { min: y, max: m } = a;
    return o.slice(y, m);
  }
  return { snapsContained: l, scrollContainLimit: a };
}
function fR(e, t, n) {
  const r = t[0],
    i = n ? r - e : Rt(t);
  return { limit: yr(i, r) };
}
function hR(e, t, n, r) {
  const s = t.min + 0.1,
    o = t.max + 0.1,
    { reachedMin: a, reachedMax: l } = yr(s, o);
  function u(f) {
    return f === 1 ? l(n.get()) : f === -1 ? a(n.get()) : !1;
  }
  function c(f) {
    if (!u(f)) return;
    const v = e * (f * -1);
    r.forEach((y) => y.add(v));
  }
  return { loop: c };
}
function pR(e) {
  const { max: t, length: n } = e;
  function r(s) {
    const o = s - t;
    return n ? o / -n : 0;
  }
  return { get: r };
}
function mR(e, t, n, r, i) {
  const { startEdge: s, endEdge: o } = e,
    { groupSlides: a } = i,
    l = d().map(t.measure),
    u = f(),
    c = v();
  function d() {
    return a(r)
      .map((m) => Rt(m)[o] - m[0][s])
      .map(le);
  }
  function f() {
    return r.map((m) => n[s] - m[s]).map((m) => -le(m));
  }
  function v() {
    return a(u)
      .map((m) => m[0])
      .map((m, x) => m + l[x]);
  }
  return { snaps: u, snapsAligned: c };
}
function gR(e, t, n, r, i, s) {
  const { groupSlides: o } = i,
    { min: a, max: l } = r,
    u = c();
  function c() {
    const f = o(s),
      v = !e || t === "keepSnaps";
    return n.length === 1
      ? [s]
      : v
      ? f
      : f.slice(a, l).map((y, m, x) => {
          const h = !m,
            p = jd(x, m);
          if (h) {
            const g = Rt(x[0]) + 1;
            return _p(g);
          }
          if (p) {
            const g = Os(s) - Rt(x)[0] + 1;
            return _p(g, Rt(x)[0]);
          }
          return y;
        });
  }
  return { slideRegistry: u };
}
function yR(e, t, n, r, i) {
  const { reachedAny: s, removeOffset: o, constrain: a } = r;
  function l(y) {
    return y.concat().sort((m, x) => le(m) - le(x))[0];
  }
  function u(y) {
    const m = e ? o(y) : a(y),
      x = t
        .map((p, g) => ({ diff: c(p - m, 0), index: g }))
        .sort((p, g) => le(p.diff) - le(g.diff)),
      { index: h } = x[0];
    return { index: h, distance: m };
  }
  function c(y, m) {
    const x = [y, y + n, y - n];
    if (!e) return y;
    if (!m) return l(x);
    const h = x.filter((p) => Od(p) === m);
    return h.length ? l(h) : Rt(x) - n;
  }
  function d(y, m) {
    const x = t[y] - i.get(),
      h = c(x, m);
    return { index: y, distance: h };
  }
  function f(y, m) {
    const x = i.get() + y,
      { index: h, distance: p } = u(x),
      g = !e && s(x);
    if (!m || g) return { index: h, distance: y };
    const S = t[h] - p,
      C = y + c(S, 0);
    return { index: h, distance: C };
  }
  return { byDistance: f, byIndex: d, shortcut: c };
}
function vR(e, t, n, r, i, s, o) {
  function a(d) {
    const f = d.distance,
      v = d.index !== t.get();
    s.add(f),
      f && (r.duration() ? e.start() : (e.update(), e.render(1), e.update())),
      v && (n.set(t.get()), t.set(d.index), o.emit("select"));
  }
  function l(d, f) {
    const v = i.byDistance(d, f);
    a(v);
  }
  function u(d, f) {
    const v = t.clone().set(d),
      y = i.byIndex(v.get(), f);
    a(y);
  }
  return { distance: l, index: u };
}
function xR(e, t, n, r, i, s, o, a) {
  const l = { passive: !0, capture: !0 };
  let u = 0;
  function c(v) {
    if (!a) return;
    function y(m) {
      if (new Date().getTime() - u > 10) return;
      o.emit("slideFocusStart"), (e.scrollLeft = 0);
      const p = n.findIndex((g) => g.includes(m));
      Ld(p) && (i.useDuration(0), r.index(p, 0), o.emit("slideFocus"));
    }
    s.add(document, "keydown", d, !1),
      t.forEach((m, x) => {
        s.add(
          m,
          "focus",
          (h) => {
            (Oa(a) || a(v, h)) && y(x);
          },
          l
        );
      });
  }
  function d(v) {
    v.code === "Tab" && (u = new Date().getTime());
  }
  return { init: c };
}
function ji(e) {
  let t = e;
  function n() {
    return t;
  }
  function r(l) {
    t = o(l);
  }
  function i(l) {
    t += o(l);
  }
  function s(l) {
    t -= o(l);
  }
  function o(l) {
    return Ld(l) ? l : l.get();
  }
  return { get: n, set: r, add: i, subtract: s };
}
function H0(e, t) {
  const n = e.scroll === "x" ? s : o,
    r = t.style;
  let i = !1;
  function s(d) {
    return `translate3d(${d}px,0px,0px)`;
  }
  function o(d) {
    return `translate3d(0px,${d}px,0px)`;
  }
  function a(d) {
    i || (r.transform = n(e.direction(d)));
  }
  function l(d) {
    i = !d;
  }
  function u() {
    i ||
      ((r.transform = ""),
      t.getAttribute("style") || t.removeAttribute("style"));
  }
  return { clear: u, to: a, toggleActive: l };
}
function wR(e, t, n, r, i, s, o, a, l) {
  const c = ws(i),
    d = ws(i).reverse(),
    f = h().concat(p());
  function v(T, E) {
    return T.reduce((D, N) => D - i[N], E);
  }
  function y(T, E) {
    return T.reduce((D, N) => (v(D, E) > 0 ? D.concat([N]) : D), []);
  }
  function m(T) {
    return s.map((E, D) => ({
      start: E - r[D] + 0.5 + T,
      end: E + t - 0.5 + T,
    }));
  }
  function x(T, E, D) {
    const N = m(E);
    return T.map((j) => {
      const I = D ? 0 : -n,
        Z = D ? n : 0,
        b = D ? "end" : "start",
        H = N[j][b];
      return {
        index: j,
        loopPoint: H,
        slideLocation: ji(-1),
        translate: H0(e, l[j]),
        target: () => (a.get() > H ? I : Z),
      };
    });
  }
  function h() {
    const T = o[0],
      E = y(d, T);
    return x(E, n, !1);
  }
  function p() {
    const T = t - o[0] - 1,
      E = y(c, T);
    return x(E, -n, !0);
  }
  function g() {
    return f.every(({ index: T }) => {
      const E = c.filter((D) => D !== T);
      return v(E, t) <= 0.1;
    });
  }
  function S() {
    f.forEach((T) => {
      const { target: E, translate: D, slideLocation: N } = T,
        j = E();
      j !== N.get() && (D.to(j), N.set(j));
    });
  }
  function C() {
    f.forEach((T) => T.translate.clear());
  }
  return { canLoop: g, clear: C, loop: S, loopPoints: f };
}
function SR(e, t, n) {
  let r,
    i = !1;
  function s(l) {
    if (!n) return;
    function u(c) {
      for (const d of c)
        if (d.type === "childList") {
          l.reInit(), t.emit("slidesChanged");
          break;
        }
    }
    (r = new MutationObserver((c) => {
      i || ((Oa(n) || n(l, c)) && u(c));
    })),
      r.observe(e, { childList: !0 });
  }
  function o() {
    r && r.disconnect(), (i = !0);
  }
  return { init: s, destroy: o };
}
function PR(e, t, n, r) {
  const i = {};
  let s = null,
    o = null,
    a,
    l = !1;
  function u() {
    (a = new IntersectionObserver(
      (y) => {
        l ||
          (y.forEach((m) => {
            const x = t.indexOf(m.target);
            i[x] = m;
          }),
          (s = null),
          (o = null),
          n.emit("slidesInView"));
      },
      { root: e.parentElement, threshold: r }
    )),
      t.forEach((y) => a.observe(y));
  }
  function c() {
    a && a.disconnect(), (l = !0);
  }
  function d(y) {
    return Ss(i).reduce((m, x) => {
      const h = parseInt(x),
        { isIntersecting: p } = i[h];
      return ((y && p) || (!y && !p)) && m.push(h), m;
    }, []);
  }
  function f(y = !0) {
    if (y && s) return s;
    if (!y && o) return o;
    const m = d(y);
    return y && (s = m), y || (o = m), m;
  }
  return { init: u, destroy: c, get: f };
}
function CR(e, t, n, r, i, s) {
  const { measureSize: o, startEdge: a, endEdge: l } = e,
    u = n[0] && i,
    c = y(),
    d = m(),
    f = n.map(o),
    v = x();
  function y() {
    if (!u) return 0;
    const p = n[0];
    return le(t[a] - p[a]);
  }
  function m() {
    if (!u) return 0;
    const p = s.getComputedStyle(Rt(r));
    return parseFloat(p.getPropertyValue(`margin-${l}`));
  }
  function x() {
    return n
      .map((p, g, S) => {
        const C = !g,
          k = jd(S, g);
        return C ? f[g] + c : k ? f[g] + d : S[g + 1][a] - p[a];
      })
      .map(le);
  }
  return { slideSizes: f, slideSizesWithGaps: v, startGap: c, endGap: d };
}
function ER(e, t, n, r, i, s, o, a, l) {
  const { startEdge: u, endEdge: c, direction: d } = e,
    f = Ld(n);
  function v(h, p) {
    return ws(h)
      .filter((g) => g % p === 0)
      .map((g) => h.slice(g, g + p));
  }
  function y(h) {
    return h.length
      ? ws(h)
          .reduce((p, g, S) => {
            const C = Rt(p) || 0,
              k = C === 0,
              T = g === Os(h),
              E = i[u] - s[C][u],
              D = i[u] - s[g][c],
              N = !r && k ? d(o) : 0,
              j = !r && T ? d(a) : 0,
              I = le(D - j - (E + N));
            return S && I > t + l && p.push(g), T && p.push(h.length), p;
          }, [])
          .map((p, g, S) => {
            const C = Math.max(S[g - 1] || 0);
            return h.slice(C, p);
          })
      : [];
  }
  function m(h) {
    return f ? v(h, n) : y(h);
  }
  return { groupSlides: m };
}
function TR(e, t, n, r, i, s, o) {
  const {
      align: a,
      axis: l,
      direction: u,
      startIndex: c,
      loop: d,
      duration: f,
      dragFree: v,
      dragThreshold: y,
      inViewThreshold: m,
      slidesToScroll: x,
      skipSnaps: h,
      containScroll: p,
      watchResize: g,
      watchSlides: S,
      watchDrag: C,
      watchFocus: k,
    } = s,
    T = 2,
    E = oR(),
    D = E.measure(t),
    N = n.map(E.measure),
    j = rR(l, u),
    I = j.measureSize(D),
    Z = aR(I),
    b = tR(a, I),
    H = !d && !!p,
    G = d || !!p,
    {
      slideSizes: B,
      slideSizesWithGaps: R,
      startGap: L,
      endGap: F,
    } = CR(j, D, N, n, G, i),
    z = ER(j, I, x, d, D, N, L, F, T),
    { snaps: Q, snapsAligned: xe } = mR(j, b, D, N, z),
    ge = -Rt(Q) + Rt(R),
    { snapsContained: Ut, scrollContainLimit: Ye } = dR(I, ge, xe, p, T),
    Pe = H ? Ut : xe,
    { limit: _e } = fR(ge, Pe, d),
    $t = W0(Os(Pe), c, d),
    lt = $t.clone(),
    se = ws(n),
    _ = (
      {
        dragHandler: dn,
        scrollBody: _a,
        scrollBounds: Va,
        options: { loop: js },
      },
      za
    ) => {
      js || Va.constrain(dn.pointerDown()), _a.seek(za);
    },
    J = (
      {
        scrollBody: dn,
        translate: _a,
        location: Va,
        offsetLocation: js,
        scrollLooper: za,
        slideLooper: G0,
        dragHandler: q0,
        animation: X0,
        eventHandler: Bd,
        scrollBounds: Y0,
        options: { loop: Ud },
      },
      $d
    ) => {
      const Wd = dn.settled(),
        Z0 = !Y0.shouldConstrain(),
        Hd = Ud ? Wd : Wd && Z0;
      Hd && !q0.pointerDown() && (X0.stop(), Bd.emit("settle")),
        Hd || Bd.emit("scroll");
      const J0 = Va.get() * $d + un.get() * (1 - $d);
      js.set(J0), Ud && (za.loop(dn.direction()), G0.loop()), _a.to(js.get());
    },
    ye = nR(
      r,
      i,
      (dn) => _(Fa, dn),
      (dn) => J(Fa, dn)
    ),
    Ve = 0.68,
    Dt = Pe[$t.get()],
    Wt = ji(Dt),
    un = ji(Dt),
    cn = ji(Dt),
    Qn = ji(Dt),
    yi = uR(Wt, cn, un, Qn, f, Ve),
    ja = yR(d, Pe, ge, _e, Qn),
    Ia = vR(ye, $t, lt, yi, ja, Qn, o),
    _d = pR(_e),
    Vd = Ps(),
    K0 = PR(t, n, o, m),
    { slideRegistry: zd } = gR(H, p, Pe, Ye, z, se),
    Q0 = xR(e, n, zd, Ia, yi, Vd, o, k),
    Fa = {
      ownerDocument: r,
      ownerWindow: i,
      eventHandler: o,
      containerRect: D,
      slideRects: N,
      animation: ye,
      axis: j,
      dragHandler: iR(
        j,
        e,
        r,
        i,
        Qn,
        sR(j, i),
        Wt,
        ye,
        Ia,
        yi,
        ja,
        $t,
        o,
        Z,
        v,
        y,
        h,
        Ve,
        C
      ),
      eventStore: Vd,
      percentOfView: Z,
      index: $t,
      indexPrevious: lt,
      limit: _e,
      location: Wt,
      offsetLocation: cn,
      previousLocation: un,
      options: s,
      resizeHandler: lR(t, o, i, n, j, g, E),
      scrollBody: yi,
      scrollBounds: cR(_e, cn, Qn, yi, Z),
      scrollLooper: hR(ge, _e, cn, [Wt, cn, un, Qn]),
      scrollProgress: _d,
      scrollSnapList: Pe.map(_d.get),
      scrollSnaps: Pe,
      scrollTarget: ja,
      scrollTo: Ia,
      slideLooper: wR(j, I, ge, B, R, Q, Pe, cn, n),
      slideFocus: Q0,
      slidesHandler: SR(t, o, S),
      slidesInView: K0,
      slideIndexes: se,
      slideRegistry: zd,
      slidesToScroll: z,
      target: Qn,
      translate: H0(j, t),
    };
  return Fa;
}
function kR() {
  let e = {},
    t;
  function n(u) {
    t = u;
  }
  function r(u) {
    return e[u] || [];
  }
  function i(u) {
    return r(u).forEach((c) => c(t, u)), l;
  }
  function s(u, c) {
    return (e[u] = r(u).concat([c])), l;
  }
  function o(u, c) {
    return (e[u] = r(u).filter((d) => d !== c)), l;
  }
  function a() {
    e = {};
  }
  const l = { init: n, emit: i, off: o, on: s, clear: a };
  return l;
}
const AR = {
  align: "center",
  axis: "x",
  container: null,
  slides: null,
  containScroll: "trimSnaps",
  direction: "ltr",
  slidesToScroll: 1,
  inViewThreshold: 0,
  breakpoints: {},
  dragFree: !1,
  dragThreshold: 10,
  loop: !1,
  skipSnaps: !1,
  duration: 25,
  startIndex: 0,
  active: !0,
  watchDrag: !0,
  watchResize: !0,
  watchSlides: !0,
  watchFocus: !0,
};
function RR(e) {
  function t(s, o) {
    return $0(s, o || {});
  }
  function n(s) {
    const o = s.breakpoints || {},
      a = Ss(o)
        .filter((l) => e.matchMedia(l).matches)
        .map((l) => o[l])
        .reduce((l, u) => t(l, u), {});
    return t(s, a);
  }
  function r(s) {
    return s
      .map((o) => Ss(o.breakpoints || {}))
      .reduce((o, a) => o.concat(a), [])
      .map(e.matchMedia);
  }
  return { mergeOptions: t, optionsAtMedia: n, optionsMediaQueries: r };
}
function MR(e) {
  let t = [];
  function n(s, o) {
    return (
      (t = o.filter(({ options: a }) => e.optionsAtMedia(a).active !== !1)),
      t.forEach((a) => a.init(s, e)),
      o.reduce((a, l) => Object.assign(a, { [l.name]: l }), {})
    );
  }
  function r() {
    t = t.filter((s) => s.destroy());
  }
  return { init: n, destroy: r };
}
function ia(e, t, n) {
  const r = e.ownerDocument,
    i = r.defaultView,
    s = RR(i),
    o = MR(s),
    a = Ps(),
    l = kR(),
    { mergeOptions: u, optionsAtMedia: c, optionsMediaQueries: d } = s,
    { on: f, off: v, emit: y } = l,
    m = j;
  let x = !1,
    h,
    p = u(AR, ia.globalOptions),
    g = u(p),
    S = [],
    C,
    k,
    T;
  function E() {
    const { container: se, slides: _ } = g;
    k = (qu(se) ? e.querySelector(se) : se) || e.children[0];
    const ye = qu(_) ? k.querySelectorAll(_) : _;
    T = [].slice.call(ye || k.children);
  }
  function D(se) {
    const _ = TR(e, k, T, r, i, se, l);
    if (se.loop && !_.slideLooper.canLoop()) {
      const J = Object.assign({}, se, { loop: !1 });
      return D(J);
    }
    return _;
  }
  function N(se, _) {
    x ||
      ((p = u(p, se)),
      (g = c(p)),
      (S = _ || S),
      E(),
      (h = D(g)),
      d([p, ...S.map(({ options: J }) => J)]).forEach((J) =>
        a.add(J, "change", j)
      ),
      g.active &&
        (h.translate.to(h.location.get()),
        h.animation.init(),
        h.slidesInView.init(),
        h.slideFocus.init(lt),
        h.eventHandler.init(lt),
        h.resizeHandler.init(lt),
        h.slidesHandler.init(lt),
        h.options.loop && h.slideLooper.loop(),
        k.offsetParent && T.length && h.dragHandler.init(lt),
        (C = o.init(lt, S))));
  }
  function j(se, _) {
    const J = z();
    I(), N(u({ startIndex: J }, se), _), l.emit("reInit");
  }
  function I() {
    h.dragHandler.destroy(),
      h.eventStore.clear(),
      h.translate.clear(),
      h.slideLooper.clear(),
      h.resizeHandler.destroy(),
      h.slidesHandler.destroy(),
      h.slidesInView.destroy(),
      h.animation.destroy(),
      o.destroy(),
      a.clear();
  }
  function Z() {
    x || ((x = !0), a.clear(), I(), l.emit("destroy"), l.clear());
  }
  function b(se, _, J) {
    !g.active ||
      x ||
      (h.scrollBody.useBaseFriction().useDuration(_ === !0 ? 0 : g.duration),
      h.scrollTo.index(se, J || 0));
  }
  function H(se) {
    const _ = h.index.add(1).get();
    b(_, se, -1);
  }
  function G(se) {
    const _ = h.index.add(-1).get();
    b(_, se, 1);
  }
  function B() {
    return h.index.add(1).get() !== z();
  }
  function R() {
    return h.index.add(-1).get() !== z();
  }
  function L() {
    return h.scrollSnapList;
  }
  function F() {
    return h.scrollProgress.get(h.location.get());
  }
  function z() {
    return h.index.get();
  }
  function Q() {
    return h.indexPrevious.get();
  }
  function xe() {
    return h.slidesInView.get();
  }
  function ge() {
    return h.slidesInView.get(!1);
  }
  function Ut() {
    return C;
  }
  function Ye() {
    return h;
  }
  function Pe() {
    return e;
  }
  function _e() {
    return k;
  }
  function $t() {
    return T;
  }
  const lt = {
    canScrollNext: B,
    canScrollPrev: R,
    containerNode: _e,
    internalEngine: Ye,
    destroy: Z,
    off: v,
    on: f,
    emit: y,
    plugins: Ut,
    previousScrollSnap: Q,
    reInit: m,
    rootNode: Pe,
    scrollNext: H,
    scrollPrev: G,
    scrollProgress: F,
    scrollSnapList: L,
    scrollTo: b,
    selectedScrollSnap: z,
    slideNodes: $t,
    slidesInView: xe,
    slidesNotInView: ge,
  };
  return N(t, n), setTimeout(() => l.emit("init"), 0), lt;
}
ia.globalOptions = void 0;
function Id(e = {}, t = []) {
  const n = w.useRef(e),
    r = w.useRef(t),
    [i, s] = w.useState(),
    [o, a] = w.useState(),
    l = w.useCallback(() => {
      i && i.reInit(n.current, r.current);
    }, [i]);
  return (
    w.useEffect(() => {
      bd(n.current, e) || ((n.current = e), l());
    }, [e, l]),
    w.useEffect(() => {
      JA(r.current, t) || ((r.current = t), l());
    }, [t, l]),
    w.useEffect(() => {
      if (ZA() && o) {
        ia.globalOptions = Id.globalOptions;
        const u = ia(o, n.current, r.current);
        return s(u), () => u.destroy();
      } else s(void 0);
    }, [o, s]),
    [a, i]
  );
}
Id.globalOptions = void 0;
const DR = {
  active: !0,
  breakpoints: {},
  delay: 4e3,
  jump: !1,
  playOnInit: !0,
  stopOnFocusIn: !0,
  stopOnInteraction: !0,
  stopOnMouseEnter: !1,
  stopOnLastSnap: !1,
  rootNode: null,
};
function NR(e, t) {
  const n = e.scrollSnapList();
  return typeof t == "number" ? n.map(() => t) : t(n, e);
}
function bR(e, t) {
  const n = e.rootNode();
  return (t && t(n)) || n;
}
function Fd(e = {}) {
  let t,
    n,
    r,
    i,
    s = null,
    o = 0,
    a = !1,
    l = !1,
    u = !1,
    c = !1;
  function d(b, H) {
    n = b;
    const { mergeOptions: G, optionsAtMedia: B } = H,
      R = G(DR, Fd.globalOptions),
      L = G(R, e);
    if (((t = B(L)), n.scrollSnapList().length <= 1)) return;
    (c = t.jump), (r = !1), (i = NR(n, t.delay));
    const { eventStore: F, ownerDocument: z } = n.internalEngine(),
      Q = !!n.internalEngine().options.watchDrag,
      xe = bR(n, t.rootNode);
    F.add(z, "visibilitychange", h),
      Q && n.on("pointerDown", g),
      Q && !t.stopOnInteraction && n.on("pointerUp", S),
      t.stopOnMouseEnter && F.add(xe, "mouseenter", C),
      t.stopOnMouseEnter && !t.stopOnInteraction && F.add(xe, "mouseleave", k),
      t.stopOnFocusIn && n.on("slideFocusStart", x),
      t.stopOnFocusIn &&
        !t.stopOnInteraction &&
        F.add(n.containerNode(), "focusout", m),
      t.playOnInit && m();
  }
  function f() {
    n.off("pointerDown", g).off("pointerUp", S).off("slideFocusStart", x),
      x(),
      (r = !0),
      (a = !1);
  }
  function v() {
    const { ownerWindow: b } = n.internalEngine();
    b.clearTimeout(o),
      (o = b.setTimeout(j, i[n.selectedScrollSnap()])),
      (s = new Date().getTime()),
      n.emit("autoplay:timerset");
  }
  function y() {
    const { ownerWindow: b } = n.internalEngine();
    b.clearTimeout(o), (o = 0), (s = null), n.emit("autoplay:timerstopped");
  }
  function m() {
    if (!r) {
      if (p()) {
        u = !0;
        return;
      }
      a || n.emit("autoplay:play"), v(), (a = !0);
    }
  }
  function x() {
    r || (a && n.emit("autoplay:stop"), y(), (a = !1));
  }
  function h() {
    if (p()) return (u = a), x();
    u && m();
  }
  function p() {
    const { ownerDocument: b } = n.internalEngine();
    return b.visibilityState === "hidden";
  }
  function g() {
    l || x();
  }
  function S() {
    l || m();
  }
  function C() {
    (l = !0), x();
  }
  function k() {
    (l = !1), m();
  }
  function T(b) {
    typeof b < "u" && (c = b), m();
  }
  function E() {
    a && x();
  }
  function D() {
    a && m();
  }
  function N() {
    return a;
  }
  function j() {
    const { index: b } = n.internalEngine(),
      H = b.clone().add(1).get(),
      G = n.scrollSnapList().length - 1,
      B = t.stopOnLastSnap && H === G;
    if (
      (n.canScrollNext() ? n.scrollNext(c) : n.scrollTo(0, c),
      n.emit("autoplay:select"),
      B)
    )
      return x();
    m();
  }
  function I() {
    if (!s) return null;
    const b = i[n.selectedScrollSnap()],
      H = new Date().getTime() - s;
    return b - H;
  }
  return {
    name: "autoplay",
    options: e,
    init: d,
    destroy: f,
    play: T,
    stop: E,
    reset: D,
    isPlaying: N,
    timeUntilNext: I,
  };
}
Fd.globalOptions = void 0;
const LR = [
  {
    src: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='800' height='400' viewBox='0 0 800 400'%3E%3Crect width='800' height='400' fill='%23004466'/%3E%3Cpath d='M0 0h800v400H0z' fill='url(%23a)'/%3E%3ClinearGradient id='a' gradientUnits='userSpaceOnUse' x1='0' y1='0' x2='800' y2='400'%3E%3Cstop offset='0' stop-color='%23005577'/%3E%3Cstop offset='1' stop-color='%23004466'/%3E%3C/linearGradient%3E%3C/svg%3E",
    alt: "Aerospace components",
  },
  {
    src: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='800' height='400' viewBox='0 0 800 400'%3E%3Crect width='800' height='400' fill='%23005588'/%3E%3Cpath d='M0 0h800v400H0z' fill='url(%23b)'/%3E%3ClinearGradient id='b' gradientUnits='userSpaceOnUse' x1='800' y1='400' x2='0' y2='0'%3E%3Cstop offset='0' stop-color='%23006699'/%3E%3Cstop offset='1' stop-color='%23005588'/%3E%3C/linearGradient%3E%3C/svg%3E",
    alt: "Precision components",
  },
  {
    src: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='800' height='400' viewBox='0 0 800 400'%3E%3Crect width='800' height='400' fill='%23006699'/%3E%3Cpath d='M0 0h800v400H0z' fill='url(%23c)'/%3E%3ClinearGradient id='c' gradientUnits='userSpaceOnUse' x1='0' y1='400' x2='800' y2='0'%3E%3Cstop offset='0' stop-color='%230077AA'/%3E%3Cstop offset='1' stop-color='%23006699'/%3E%3C/linearGradient%3E%3C/svg%3E",
    alt: "Technical expertise",
  },
];
function OR() {
  const [e, t] = Id({ loop: !0 }, [Fd({ delay: 5e3, stopOnInteraction: !1 })]),
    n = w.useCallback(() => {
      t && (console.log("Scrolling to previous slide"), t.scrollPrev());
    }, [t]),
    r = w.useCallback(() => {
      t && (console.log("Scrolling to next slide"), t.scrollNext());
    }, [t]);
  return (
    w.useEffect(() => {
      t && console.log("Carousel initialized");
    }, [t]),
    P.jsx("section", {
      className: "pt-24 pb-12 md:pt-32 md:pb-20",
      children: P.jsx("div", {
        className: "container mx-auto px-4",
        children: P.jsxs("div", {
          className: "grid md:grid-cols-2 gap-12 items-center",
          children: [
            P.jsxs(ra.div, {
              initial: { opacity: 0, y: 20 },
              animate: { opacity: 1, y: 0 },
              transition: { duration: 0.6 },
              children: [
                P.jsxs("h1", {
                  className:
                    "text-4xl md:text-5xl font-bold text-foreground mb-6",
                  children: [
                    "Expert Aerospace",
                    " ",
                    P.jsx("span", {
                      className: "text-primary",
                      children: "Elastomer Component",
                    }),
                    " MRO Services",
                  ],
                }),
                P.jsx("p", {
                  className: "text-lg text-muted-foreground mb-4",
                  children:
                    "Specialized re-molding of aerospace plate seals, R&O services for diaphragms, diaphragm assemblies, and other elastomer components. Industry-leading quality and rapid turnaround times.",
                }),
                P.jsx("p", {
                  className: "text-lg text-muted-foreground mb-8",
                  children:
                    "Serving airline, OEM, MRO, and military customers.",
                }),
                P.jsxs("div", {
                  className: "flex flex-col sm:flex-row gap-4",
                  children: [
                    P.jsx(nr, {
                      size: "lg",
                      asChild: !0,
                      children: P.jsx("a", {
                        href: "mailto:rfq@asdmro.com?subject=ASD%20MRO%20RFQ",
                        children: "Request Quote",
                      }),
                    }),
                    P.jsx(nr, {
                      size: "lg",
                      variant: "outline",
                      asChild: !0,
                      children: P.jsx("a", {
                        href: "#services",
                        children: "Our Services",
                      }),
                    }),
                  ],
                }),
              ],
            }),
            P.jsx(ra.div, {
              initial: { opacity: 0, scale: 0.95 },
              animate: { opacity: 1, scale: 1 },
              transition: { duration: 0.6, delay: 0.2 },
              className: "relative overflow-hidden rounded-lg shadow-lg",
              children: P.jsxs("div", {
                className: "relative",
                children: [
                  P.jsx("div", {
                    className: "overflow-hidden",
                    ref: e,
                    children: P.jsx("div", {
                      className: "flex",
                      children: LR.map((i, s) =>
                        P.jsx(
                          "div",
                          {
                            className: "flex-[0_0_100%] min-w-0",
                            children: P.jsx("div", {
                              className: "aspect-video relative",
                              children: P.jsx("img", {
                                src: i.src,
                                alt: i.alt,
                                className: "object-cover w-full h-full",
                              }),
                            }),
                          },
                          s
                        )
                      ),
                    }),
                  }),
                  P.jsx(nr, {
                    variant: "outline",
                    size: "icon",
                    className:
                      "absolute left-4 top-1/2 -translate-y-1/2 z-50 bg-white hover:bg-white/90 shadow-lg p-3",
                    onClick: n,
                    "aria-label": "Previous slide",
                    children: P.jsx(LP, { className: "h-6 w-6" }),
                  }),
                  P.jsx(nr, {
                    variant: "outline",
                    size: "icon",
                    className:
                      "absolute right-4 top-1/2 -translate-y-1/2 z-50 bg-white hover:bg-white/90 shadow-lg p-3",
                    onClick: r,
                    "aria-label": "Next slide",
                    children: P.jsx(OP, { className: "h-6 w-6" }),
                  }),
                ],
              }),
            }),
          ],
        }),
      }),
    })
  );
}
const jR = [
  {
    title: "Seal Repair & Overhaul",
    description:
      "Comprehensive repair and overhaul services for all types of aerospace seals including hydraulic, pneumatic, and static seals.",
    icon: UP,
  },
  {
    title: "Diaphragm Assembly Services",
    description:
      "Expert assembly, restoration and testing of aerospace diaphragms, ensuring optimal performance and reliability.",
    icon: BP,
  },
  {
    title: "Rapid Turnaround",
    description:
      "Industry-leading turnaround times without compromising on quality or reliability.",
    icon: IP,
  },
  {
    title: "Certified Quality",
    description:
      "All services performed to aerospace standards with full documentation and traceability.",
    icon: tv,
  },
];
function IR() {
  return P.jsx("section", {
    id: "services",
    className: "py-20 bg-gray-50",
    children: P.jsxs("div", {
      className: "container mx-auto px-4",
      children: [
        P.jsxs("div", {
          className: "text-center mb-12",
          children: [
            P.jsx("h2", {
              className: "text-3xl font-bold mb-4",
              children: "Services",
            }),
            P.jsx("p", {
              className: "text-lg text-muted-foreground max-w-2xl mx-auto",
              children:
                "Comprehensive MRO solutions for aerospace elastomer components, delivering quality and reliability for critical applications.",
            }),
          ],
        }),
        P.jsx("div", {
          className: "grid md:grid-cols-2 lg:grid-cols-4 gap-6",
          children: jR.map((e, t) =>
            P.jsx(
              ra.div,
              {
                initial: { opacity: 0, y: 20 },
                whileInView: { opacity: 1, y: 0 },
                transition: { duration: 0.5, delay: t * 0.1 },
                viewport: { once: !0 },
                className: "h-full",
                children: P.jsxs(Aa, {
                  className: "h-full flex flex-col",
                  children: [
                    P.jsxs(pv, {
                      children: [
                        P.jsx(e.icon, {
                          className: "h-10 w-10 text-primary mb-4",
                        }),
                        P.jsx(mv, { children: e.title }),
                      ],
                    }),
                    P.jsx(Ra, {
                      className: "flex-grow",
                      children: P.jsx("p", {
                        className: "text-muted-foreground",
                        children: e.description,
                      }),
                    }),
                  ],
                }),
              },
              e.title
            )
          ),
        }),
      ],
    }),
  });
}
function FR() {
  return (
    w.useEffect(() => {
      const e = document.createElement("script");
      return (
        (e.src = "//js.hsforms.net/forms/embed/v2.js"),
        (e.charset = "utf-8"),
        (e.type = "text/javascript"),
        document.head.appendChild(e),
        (e.onload = () => {
          window.hbspt &&
            window.hbspt.forms.create({
              portalId: "8226801",
              formId: "00106bf5-cb01-4537-bd7b-20e3ef798278",
              target: "#hubspot-form",
              region: "na1",
            });
        }),
        () => {
          const t = document.querySelector(
            'script[src="//js.hsforms.net/forms/embed/v2.js"]'
          );
          t && t.parentNode && t.parentNode.removeChild(t);
          const n = document.getElementById("hubspot-form");
          n && (n.innerHTML = "");
        }
      );
    }, []),
    P.jsx("section", {
      id: "contact",
      className: "py-20 bg-gray-50",
      children: P.jsx("div", {
        className: "container mx-auto px-4",
        children: P.jsxs("div", {
          className: "max-w-2xl mx-auto",
          children: [
            P.jsxs("div", {
              className: "text-center mb-12",
              children: [
                P.jsx("h2", {
                  className: "text-3xl font-bold mb-4",
                  children: "Contact Us",
                }),
                P.jsx("p", {
                  className: "text-lg text-muted-foreground",
                  children:
                    "Get in touch for quotes, inquiries, or to learn more about our services.",
                }),
              ],
            }),
            P.jsx("div", {
              id: "hubspot-form",
              className: "mt-8 bg-white p-6 rounded-lg shadow-sm",
            }),
          ],
        }),
      }),
    })
  );
}
const _R = [
  {
    title: "AS9100D",
    description:
      "Quality Management System certification specific to aerospace, space and defense organizations",
  },
  {
    title: "ISO 9001:2015",
    description: "International standard for quality management systems",
  },
  {
    title: "NADCAP",
    description:
      "National Aerospace and Defense Contractors Accreditation Program for elastomer seals",
  },
  {
    title: "FAA Part 145",
    description: "Federal Aviation Administration repair station certification",
  },
  {
    title: "EASA",
    description: "European Union Aviation Safety Agency certification",
  },
  {
    title: "Drug & Alcohol Program",
    description: "Anti-Drug and Alcohol Misuse Prevention Program compliant",
  },
];
function VR() {
  return P.jsx("section", {
    id: "certifications",
    className: "py-20",
    children: P.jsxs("div", {
      className: "container mx-auto px-4",
      children: [
        P.jsxs("div", {
          className: "text-center mb-12",
          children: [
            P.jsx("h2", {
              className: "text-3xl font-bold mb-4",
              children: "Certifications",
            }),
            P.jsx("p", {
              className: "text-lg text-muted-foreground max-w-2xl mx-auto",
              children:
                "Maintaining the highest industry standards and certifications to ensure quality and reliabilityyyy in all services.",
            }),
          ],
        }),
        P.jsx("div", {
          className: "grid md:grid-cols-3 gap-6",
          children: _R.map((e, t) =>
            P.jsx(
              ra.div,
              {
                initial: { opacity: 0, scale: 0.95 },
                whileInView: { opacity: 1, scale: 1 },
                transition: { duration: 0.5, delay: t * 0.1 },
                viewport: { once: !0 },
                className: "h-full",
                children: P.jsx(Aa, {
                  className: "h-full flex flex-col",
                  children: P.jsxs(Ra, {
                    className:
                      "pt-6 flex-grow flex flex-col items-center justify-center",
                    children: [
                      P.jsx(tv, { className: "h-12 w-12 text-primary mb-4" }),
                      P.jsx("h3", {
                        className: "text-xl font-semibold mb-2",
                        children: e.title,
                      }),
                      P.jsx("p", {
                        className: "text-muted-foreground text-center",
                        children: e.description,
                      }),
                    ],
                  }),
                }),
              },
              e.title
            )
          ),
        }),
      ],
    }),
  });
}
function zR() {
  return P.jsxs("div", {
    className: "min-h-screen bg-background",
    children: [
      P.jsx(DC, {}),
      P.jsxs("main", {
        children: [P.jsx(OR, {}), P.jsx(IR, {}), P.jsx(VR, {}), P.jsx(FR, {})],
      }),
      P.jsx(NC, {}),
    ],
  });
}
function BR() {
  return P.jsxs(iS, {
    children: [
      P.jsx(lh, { path: "/", component: zR }),
      P.jsx(lh, { component: RC }),
    ],
  });
}
function UR() {
  return P.jsxs(RS, { client: NS, children: [P.jsx(BR, {}), P.jsx(TC, {})] });
}
oy(document.getElementById("root")).render(P.jsx(UR, {}));
